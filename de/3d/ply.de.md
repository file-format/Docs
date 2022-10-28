{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "Datei", "Erweiterung", "Format", "3D-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das PLY-Dateiformat und APIs, die PLY-Dateien erstellen und öffnen können.",
  "title" :"PLY - Polygon 3D-Dateiformat",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PLY-Datei?

PLY, Polygon File Format, stellt ein 3D-Dateiformat dar, das grafische Objekte speichert, die als eine Sammlung von Polygonen beschrieben werden. Der Zweck dieses Dateiformats bestand darin, einen einfachen und einfachen Dateityp zu etablieren, der allgemein genug ist, um für eine Vielzahl von Modellen nützlich zu sein. Das PLY-Dateiformat ist sowohl im ASCII- als auch im Binärformat für kompakte Speicherung und schnelles Speichern und Laden verfügbar. Das Dateiformat wird von verschiedenen Anwendungen verwendet, die das Lesen von 3D-Dateien unterstützen.

Objekte im PLY-Format werden durch eine Sammlung von Scheitelpunkten, Flächen und anderen Elementen zusammen mit Eigenschaften wie Farbe und Normalenrichtung beschrieben, die diesen Elementen zugeordnet werden können. Zu den weiteren Eigenschaften, die ebenfalls mit dem Objekt gespeichert werden können, gehören:

* Oberflächennormalen
* Texturkoordinaten
* Transparenz
* Bereich Datenvertrauen
* Eigenschaften für die Vorder- und Rückseite eines Polygons

Ein durch das PLY-Format dargestelltes Objekt kann das Ergebnis verschiedener Quellen sein, wie z. B. handdigitalisierte Objekte, Polygonobjekte aus Modellierungsanwendungen, Entfernungsdaten, Dreiecke aus Marschwürfeln, Geländedaten und Radiosity-Modelle.

## Kurze Geschichte

Das PLY-Format wurde in den 1990er Jahren von Greg Turk und anderen im Grafiklabor Stanford entwickelt und ist daher auch als Stanford Triangle Format bekannt. Das Dateiformat hat seitdem die Version 1.0 und es wurden keine weiteren Änderungen vorgenommen.

## PLY-Dateiformat

Ein einfaches PLY-Objekt besteht aus einer Sammlung von Elementen zur Darstellung des Objekts. Es besteht aus einer Liste von (x,y,z)-Tripeln von Scheitelpunkten und einer Liste von Flächen, die tatsächlich Indizes in der Liste von Scheitelpunkten sind. Scheitelpunkte und Flächen sind zwei Beispiele für Elemente, und der Großteil der PLY-Datei besteht aus diesen beiden Elementen. Es können auch neue Eigenschaften erstellt und an die Elemente eines Objekts angehängt werden, aber diese sollten so hinzugefügt werden, dass alte Programme nicht abbrechen, wenn sie auf diese neuen Eigenschaften stoßen. Solche Eigenschaften können auch durch das Lesen von Anwendungen verworfen werden. Außerdem können mit diesem Element neue Elemente erstellt und Eigenschaften definiert werden.

### Dateistruktur

Die Dateistruktur eines PLY-Dateiformats sieht wie folgt aus:

|Feld
---|
|Datei-Header
|Scheitelpunktliste
|Liste der Gesichter
|Liste anderer Elemente

#### Beispielstruktur

Wir werden das folgende Beispiel unten in unserer nachfolgenden Diskussion für verschiedene Teile eines PLY-Dateiformats verwenden.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Dateikopf

Der Header des PLY-Dateiformats besteht sowohl für das ASCII- als auch für das Binärformat aus ASCII-Text. Der Anfang und das Ende des Header-Abschnitts werden durch die Schlüsselwörter ply und end-header identifiziert. Der Anfang des Headers hat das Zauberwort ply, das zur Erkennung des PLY-Dateiformats durch Leser verwendet wird. Die nächste Zeile zeigt die Versionsnummer dieser Datei. Kommentare in einem PLY-Dateiformat beginnen mit dem Kommentarschlüsselwort am Anfang jeder Kommentarzeile.

#### Elementschlüsselwort

Das Schlüsselwort element gibt dann an, was sich in der Datei befindet. Es folgen Eigenschaften für diesen spezifischen Elementtyp, wobei jede Eigenschaft ihren Eigenschaftstyp und ihre Reihenfolge wie unten gezeigt hat:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

In diesem speziellen Beispiel hat das spezifische Scheitelpunktelement 3 Eigenschaften vom Typ Float mit angegebener Reihenfolge.

#### Arten von Datentypen

Es gibt zwei Arten von Datentypen, die eine Eigenschaft haben kann.

„Skalar“: Die skalaren Datentypen sind wie folgt:


|#Name|#Typ|#Anzahl Bytes
|Zeichen|Zeichen|1
|uchar|Zeichen ohne Vorzeichen|1
|kurz|kurze Ganzzahl|2
|ushort|unsigned short integer|2
|int|Ganzzahl|4
|uint|Ganzzahl ohne Vorzeichen|4
|Float|Float mit einfacher Genauigkeit|4
|double|double precision float|8

`List`: Es gibt eine spezielle Form von Eigenschaftsdefinitionen, die den Listendatentyp verwendet. Ein Beispiel dafür ist aus der obigen Cube-Datei:

`Eigenschaftsliste uchar int vertex_index`

Das bedeutet, dass die Eigenschaft "vertex_index" zuerst ein unsigned char enthält, das angibt, wie viele Indizes die Eigenschaft enthält, gefolgt von einer Liste, die so viele ganze Zahlen enthält. Jede ganze Zahl in dieser Liste variabler Länge ist ein Index zu einem Scheitelpunkt.

## Verweise ##

* [PLY-Dateiformat](http://paulbourke.net/dataformats/ply/)
* [PLY – Von Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

