{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "Datei", "Erweiterung", "Format", "3D-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine FBX-Datei und APIs sind, die sie erstellen und öffnen können.",
  "title" :"FBX - FilmBox 3D-Dateiformat",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine FBX-Datei?

FBX, FilmBox, ist ein beliebtes 3D-Dateiformat, das ursprünglich von Kaydara für MotionBuilder entwickelt wurde. Es wurde 2006 von Autodesk Inc übernommen und ist heute eines der wichtigsten 3D-Austauschformate, das von vielen 3D-Tools verwendet wird. FBX ist sowohl im Binär- als auch im ASCII-Dateiformat verfügbar. Das Format wurde eingerichtet, um Interoperabilität zwischen Anwendungen zur Erstellung digitaler Inhalte bereitzustellen. Es gibt viele Tools für die Konvertierung vom/zum FBX-Dateiformat.

## FBX-Dateiformat - Weitere Informationen

FBX ist ein proprietäres Format und Spezifikationen über sein binäres Dateiformat sind nicht offiziell verfügbar. Ein C++ FBX SDK wird von Autodesk zum Lesen, Schreiben und Konvertieren in/aus FBX-Dateien bereitgestellt. Ein Python-Import- und Exportskript für FBX ist auch in der Blender-Software verfügbar, die das FBX-SDK nicht verwendet.

### Textbasierte Dateistruktur ###

Die textbasierte Dateistruktur ist eine baumstrukturierte Dokumentation mit eindeutig benannten Identifikatoren. Es besteht aus einer verschachtelten Liste von Knoten, die hierarchisch angeordnet sind, wobei jeder Knoten Folgendes hat:

* Ein NodeType-Bezeichner (Klassenname)
* Ein Tupel von damit verbundenen Eigenschaften, die Tupelelemente sind die üblichen primitiven Datentypen: ##float, integer, string## usw.
* Eine Liste, die Knoten im gleichen Format (rekursiv) enthält.

Diese lassen sich logisch wie folgt darstellen:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Einige der Standardknoten sind als implizite Liste definiert, wobei jedes Element aus einer verschachtelten Liste besteht. Jede Anwendung, die beabsichtigt, auf die FBX-Geometrie zuzugreifen, muss diese Inhalte parsen und eine sinnvolle Bedeutung daraus ziehen. Ein Beispiel für eine textbasierte FBX-Datei ist wie folgt:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Binäre Dateistruktur ##

Wie bereits erwähnt, sind FBX-Dateiformatspezifikationen für FBX nicht öffentlich verfügbar. Da die Blender Foundation das FBX-Dateiformat implementiert, ohne das vom Unternehmen bereitgestellte SDK zu verwenden, sind einige Details zum binären Dateiformat [verfügbar](https://code.blender.org/2013/08/fbx-binary-file-format -Spezifikation/) als Teil der Implementierung.

Die Struktur der Binärdateien folgt der folgenden Reihenfolge:

* Header
* Objektdatensatz
* Fusszeile

### Header ###

Die Dateikopfinformationen bestehen aus 27 Bytes.

* Bytes 0 - 20: Kaydara FBX Binär \x00 (Datei-Magie, mit 2 Leerzeichen am Ende, dann ein NULL-Terminator).
* Bytes 21 - 22: [0x1A, 0x00]## (unbekannt, aber alle beobachteten Dateien zeigen diese Bytes).
* Bytes 23 - 26: unsigned int, die Versionsnummer. 7300 für Version 7.3 zum Beispiel.

### Objektdatensatz ###

Dem Header folgt ein Objektdatensatz, der ein vollständiger Knotendatensatz mit leerem Namen und leerer Eigenschaftsliste ist. Es enthält rekursiv die gesamte Dateiformation.

### Fusszeile ###

Der Abschnitt FBX-Fußzeile befindet sich am Ende einer Datei, deren Inhalt unbekannt ist.

## Datensatzformate ##

Datensätze in einer FBX-Datei werden wie folgt kategorisiert:

* Knotenaufzeichnungen
* Eigentumsaufzeichnungen

### Knotendatensatzformat ###

Jedes Knotendatensatzformat ist benannt und hat das folgende Speicherlayout.


|Größe (Bytes)|Datumstyp|Name
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|AnzahlEigenschaften
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NameLänge|Zeichen|Name
|?|?|Property[n], wobei n = 0:PropertyListLen
|Optional| |
|?|?|VerschachtelteListe
|13|uint8[]|Null-Datensatz

wo:

* `EndOffset` ist der Abstand vom Anfang der Datei bis zum Ende des Node-Records (dh das erste Byte dessen, was als Nächstes kommt). Dies kann verwendet werden, um unbekannte oder nicht benötigte Datensätze einfach zu überspringen.
* „NumProperties“ ist die Anzahl der Eigenschaften im Wertetupel, das dem Knoten zugeordnet ist. Eine verschachtelte Liste als letztes Element wird nicht als Eigenschaft gezählt.
* `PropertyListLen` ist die Länge der Eigenschaftsliste. Dies ist die zum Speichern von ##NumProperties##-Eigenschaften erforderliche Größe, die vom Datentyp der Eigenschaften abhängt.
* „NameLen“ ist die Länge des Objektnamens in Zeichen. Der einzige Fall, in dem dies 0 ist, scheint die oberste Ebene der Liste zu sein.
* „Name“ ist der Name des Objekts. Es gibt keine Nullterminierung.
* `Property[n]` ist die n-te Eigenschaft. Für das Format siehe Abschnitt Eigenschaft Datensatzformat. Eigenschaften werden sequentiell und ohne Polsterung geschrieben.
* `NestedList` ist die verschachtelte Liste, deren Anwesenheit durch einen NULL–Eintrag ganz am Ende angezeigt wird.

Das Vorhandensein eines verschachtelten Listeneintrags kann festgestellt werden, indem überprüft wird, ob bis zum Erreichen des EndOffset Bytes übrig sind. Wenn dies der Fall ist, sollte der nächste Objektdatensatz direkt nach der letzten Eigenschaft gelesen werden. Dem Objektdatensatz folgen dann 13 Null-Bytes, die dann mit dem EndOffset kombiniert werden. Der Zweck oder die Anforderung des NULL-Eintrags ist nicht bekannt und kann auf ein Formatmerkmal hinweisen.

### Eigenschaftsdatensatzformat ###

Ein Eigenschaftsdatensatz enthält Details zu Eigenschaften, die Teil von Node sind. Ein Eigenschaftsdatensatz hat das folgende Speicherlayout:


|Größe (Bytes)|Datentyp|Name
--- | --- | ---
|1|Zeichen|Typencode
|?|?|Daten

TypeCode stellen Zeichencodes dar, die in Gruppen geordnet sind, die eine ähnliche Behandlung erfordern. TypeCodes können in folgende Typen kategorisiert werden und TypeCode kann einer der Zeichencodes unter diesen Typen sein.

#### Primitive Typen ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Die Daten im Datensatz des primitiven Skalartyps sind genau die binäre Darstellung des Werts in Little-Endian-Byte-Reihenfolge.

#### Array-Typen ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Die Daten für den Array-Typ sind komplexer und haben die folgende Struktur.


|Größe (Bytes)|Datentyp|Name
--- | --- | ---
|4|Uint32|Arraylänge
|4|Uint32|Codierung
|4|Uint32|Komprimierte Länge
|?|?|Inhalt

### Sondertypen ###

Es folgen die TypeCodes der Spezialtypen.

```
S: String
R: raw binary data
```

Diese beiden TypeCodes werden wie folgt dargestellt:


|Größe (Bytes)|Datentyp|Name
--- | --- | ---
|4|Uin32|Länge
|Länge| |

Die Zeichenfolge ist nicht nullterminiert und kann durchaus \0-Zeichen enthalten (dies wird tatsächlich in einigen FBX-Eigenschaften verwendet).

## Verweise ##

* [FBX – Das Autodesk-SDK] (http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [FBX-Binärdateiformatspezifikationen](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX – Wikipedia](https://en.wikipedia.org/wiki/FBX#Dateiformat)

