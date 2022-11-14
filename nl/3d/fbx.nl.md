{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "bestand", "extensie", "formaat", "3D-bestandsformaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een FBX-bestand is en API's die ze kunnen maken en openen.",
  "title" :"FBX - FilmBox 3D-bestandsindeling",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een FBX-bestand?

FBX, FilmBox, is een populair 3D-bestandsformaat dat oorspronkelijk is ontwikkeld door Kaydara voor MotionBuilder. Het werd in 2006 overgenomen door Autodesk Inc en is nu een van de belangrijkste 3D-uitwisselingsformaten die door veel 3D-tools worden gebruikt. FBX is beschikbaar in zowel binaire als ASCII-bestandsindeling. Het formaat is opgezet om interoperabiliteit te bieden tussen toepassingen voor het maken van digitale inhoud. Er zijn veel tools beschikbaar voor conversie van/naar het FBX-bestandsformaat.

## FBX-bestandsindeling - Meer informatie

FBX is een eigen formaat en specificaties over het binaire bestandsformaat zijn officieel niet beschikbaar. Een C++ FBX SDK wordt geleverd door Autodesk voor het lezen, schrijven en converteren van/naar FBX-bestanden. Een Python import- en exportscript voor FBX is ook beschikbaar in Blender-software die de FBX SDK niet gebruikt.

### Op tekst gebaseerde bestandsstructuur

De op tekst gebaseerde bestandsstructuur is een boomstructuur gedocumenteerd met duidelijk benoemde identifiers. Het bestaat uit een geneste lijst van knooppunten gerangschikt in hiërarchie waarbij elk knooppunt:

* Een NodeType-ID (klassenaam)
* Een tupel van eigenschappen die ermee verbonden zijn, de tupel-elementen zijn de gebruikelijke primitieve datatypes: ##float, integer, string## etc.
* Een lijst met knooppunten in hetzelfde formaat (recursief).

Deze kunnen logisch als volgt worden weergegeven:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Sommige standaardknooppunten zijn gedefinieerd als een impliciete lijst waarbij elk item uit een geneste lijst bestaat. Elke toepassing die toegang wil krijgen tot FBX-geometrie, moet deze inhoud ontleden en er een bruikbare betekenis aan geven. Hieronder ziet u een voorbeeld van een op tekst gebaseerd FBX-bestand:

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

## Binaire bestandsstructuur van FBX-bestanden

Zoals eerder vermeld, zijn FBX-bestandsformaatspecificaties niet openbaar beschikbaar voor FBX. Aangezien Blender Foundation het FBX-bestandsformaat implementeert zonder de door het bedrijf verstrekte SDK te gebruiken, zijn enkele details over het binaire bestandsformaat [beschikbaar](https://code.blender.org/2013/08/fbx-binary-file-format -specificatie/) als onderdeel van de implementatie ervan.

De structuur van de binaire bestanden volgt de volgende volgorde:

* Koptekst
* Objectrecord
* Voettekst

### FBX-koptekst

De bestandskopinformatie bestaat uit 27 bytes.

* Bytes 0 - 20: Kaydara FBX Binary \x00 (bestandsmagie, met 2 spaties aan het einde, dan een NULL-terminator).
* Bytes 21 - 22: [0x1A, 0x00]## (onbekend maar alle waargenomen bestanden tonen deze bytes).
* Bytes 23 - 26: unsigned int, het versienummer. 7300 voor versie 7.3 bijvoorbeeld.

### Objectrecord ###

De koptekst wordt gevolgd door een objectrecord dat een record met een volledig knooppunt is met een lege naam en een lege eigenschappenlijst. Het bevat recursief de volledige bestandsformatie.

### Voettekst ###

De sectie FBX Footer bevindt zich aan het einde van het bestand waarvan de inhoud onbekend is.

## Recordformaten ##

Records in een FBX-bestand worden gecategoriseerd als:

* Knooppuntrecords
* Eigendomsrecords

### Node Record Formaat ###

Elk Node Record Format heeft een naam en heeft de volgende geheugenlay-out.


|Grootte (bytes)|Datumtype|Naam
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|AantalEigenschappen
|4|UInt32|PropertyListLen
|1|UInt8|NaamLen
|NaamLengte|char|Naam
|?|?|Eigenschap[n], waarbij n = 0:PropertyListLen
|Optioneel| |
|?|?|NestedList
|13|uint8[]|Null-record

waar:

* `EndOffset` is de afstand van het begin van het bestand tot het einde van het knooppuntrecord (dwz de eerste byte van wat daarna komt). Dit kan worden gebruikt om onbekende of niet vereiste records gemakkelijk over te slaan.
* `NumProperties` is het aantal eigenschappen in de waarde-tupel die aan het knooppunt is gekoppeld. Een geneste lijst als laatste element wordt niet meegeteld als eigenschap.
* `PropertyListLen` is de lengte van de eigenschappenlijst. Dit is de grootte die nodig is voor het opslaan van ##NumProperties## eigenschappen, die afhangt van het gegevenstype van de eigenschappen.
* `NameLen` is de lengte van de objectnaam, in tekens. Het enige geval waarin dit 0 is, lijken de lijsten op het hoogste niveau te zijn.
* `Naam` is de naam van het object. Er is geen zero-termination.
* `Eigenschap[n]` is de zoveelste eigenschap. Voor het formaat, zie paragraaf eigenschap Recordformaat. Eigenschappen worden opeenvolgend en zonder opvulling geschreven.
* `NestedList` is de geneste lijst, waarvan de aanwezigheid helemaal aan het einde wordt aangegeven door een NULL–record.

Het bestaan van een geneste lijstitem kan worden bepaald door te controleren of er bytes over zijn totdat de EndOffset is bereikt. Als dat het geval is, moet het volgende objectrecord direct na de laatste eigenschap worden gelezen. Het objectrecord volgt dan 13 nul bytes, die vervolgens worden gecombineerd met de EndOffset. Het doel of de vereiste van de NULL-invoer is niet bekend en kan wijzen op een indelingsfunctie.

### Eigenschap Record Formaat ###

Een eigenschapsrecord bevat details over eigenschappen die deel uitmaken van Node. Een eigenschapsrecord heeft de volgende geheugenindeling:


|Grootte (bytes)|Gegevenstype|Naam
--- | --- | ---
|1|char|TypeCode
|?|?|Gegevens

TypeCode vertegenwoordigen tekencodes die zijn geordend in groepen die een vergelijkbare behandeling vereisen. TypeCodes kunnen worden onderverdeeld in de volgende typen en TypeCode kan een van de tekencodes onder deze typen zijn.

#### Primitieve typen ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Gegevens in het primitieve scalaire type record zijn precies de binaire representatie van de waarde, in de volgorde van de kleine endiane bytes.

#### Matrixtypen ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

De gegevens voor matrixtype zijn complexer en hebben de volgende structuur.


|Grootte (bytes)|Gegevenstype|Naam
--- | --- | ---
|4|Uint32|ArrayLengte
|4|Uint32|Codering
|4|Uint32|CompressedLength
|?|?|Inhoud

### Speciale soorten ###

Hieronder volgen de Special Types TypeCodes.

```
S: String
R: raw binary data
```

Beide TypeCodes worden als volgt weergegeven:


|Grootte (bytes)|Gegevenstype|Naam
--- | --- | ---
|4|Uin32|Lengte
|Lengte| |

De string heeft geen nulterminatie en kan \0 karakters bevatten (dit wordt in sommige FBX-eigenschappen gebruikt).

## Referenties ##

* [FBX - De Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [FBX binaire bestandsformaatspecificaties](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

