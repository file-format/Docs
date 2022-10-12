{
  "date" : "2019-10-11",
  "keywords" :[ "obj-Datei", "obj-Dateiformat", "was ist eine obj-Datei", "Datei", "obj-Beispiel", "obj-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ-Dateiformat",
  "description":"Erfahren Sie mehr über das OBJ-Dateiformat und APIs, die OBJ-Dateien öffnen und erstellen können.",
  "linktitle" :"OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine OBJ-Datei?

**OBJ**-Dateien werden von der Advanced Visualizer-Anwendung von Wavefront verwendet, um die geometrischen Objekte zu definieren und zu speichern. Die Rückwärts- und Vorwärtsübertragung von geometrischen Daten wird durch OBJ-Dateien ermöglicht. Sowohl polygonale Geometrie wie Punkte, Linien, Texturscheitel, Flächen als auch Freiformgeometrie (Kurven und Flächen) werden vom OBJ-Format unterstützt. Dieses Format unterstützt keine Animationen oder Informationen in Bezug auf Licht und Position von Szenen. Eine OBJ-Datei ist normalerweise ein Endprodukt des 3D-Modellierungsprozesses, der von einem CAD (Computer Aided Design) generiert wird. Die Standardreihenfolge zum Speichern von Scheitelpunkten ist gegen den Uhrzeigersinn, wodurch eine explizite Deklaration von Flächennormalen vermieden wird. Obwohl OBJ-Dateien Maßstabsinformationen in einer Kommentarzeile deklarieren, wurden für OBJ-Koordinaten keine Einheiten deklariert.

## Geschichte

Wavefront Technologies hat das OBJ-Dateiformat für seine Advanced Visualizer-Anwendung entwickelt, um geometrische Objekte und 3D-Daten zu speichern. Seine Version 2.11 wird durch eine neu dokumentierte Version 3 ersetzt. Das Dateiformat ist offen und wurde von anderen Anbietern für ihre 3D-Grafikanwendung implementiert. Wavefront Technologies hielt dieses Dateiformat Open Source und neutral.

## OBJ-Dateiformat

Bei 3D-Objekten ist die Codierung der Oberflächengeometrie eine anspruchsvolle Aufgabe, die das OBJ-Dateiformat sehr gut bewältigt hat. Dieses Format ist sehr vielseitig, da es eine Reihe von Möglichkeiten zur Codierung der Oberflächengeometrie bietet. Im Folgenden sind drei zulässige Formate aufgeführt, die ihre eigenen Vor- und Nachteile haben:

### Tessellation mit polygonalen Flächen

Das OBJ-Dateiformat erleichtert dem Benutzer das Tessellieren einer 3D-Modelloberfläche mit einfachen oder komplexen geometrischen Formen. Für die Codierung der Oberflächengeometrie eines Modells speichert eine Datei die Scheitelpunkte und Normalen zu jedem Polygon. Obwohl die Tessellation das Modell grober macht, ist es dennoch notwendig, das richtige Gleichgewicht zwischen der Größe einer Datei und ihrer Druckqualität zu finden.

### Freiformkurve

Das OBJ-Dateiformat ermöglicht es den benutzerdefinierten Freiform-Oberflächenkurven, die Oberflächengeometrie eines Modells anzugeben. Da Freiformkurven komplexer sind als Polygonflächen, können gekrümmte Linien mit wenigen mathematischen Parametern am besten durch Freiformkurven definiert werden. Daher werden Freiformkurven mit weniger Daten im Vergleich zu polygonalen Tessellationen verwendet, um eine hochwertige Codierung eines beliebigen 3D-Modells zu generieren, ohne die Dateigröße zu erweitern.

### Freiformflächen

Das OBJ-Dateiformat spezifiziert auch die Kachelung der Oberflächengeometrie mit Freiform-Oberflächenpatches. Diese Art von Freeform Surface Patches (NURBS) eignet sich sehr gut für Oberflächen ohne starre radiale Abmessungen wie die Karosserie eines Lastwagens, die Flügel eines Hubschraubers oder den Rumpf eines Bootes. Die Verwendung von Freiformflächen ist sehr vorteilhaft, da sie präziser sind, um die Dateigröße bei höherer Genauigkeit kleiner zu halten. Diese Oberflächen sind ein wesentlicher Bestandteil der Luft- und Raumfahrt- und Automobilindustrie, wo die geringe Präzision unversöhnlich ist.

Die folgenden Schlüsselwörter sind nach Datentyp angeordnet, um die Oberflächengeometrie zu definieren.


|Elemente|Freiformkurven-/Flächenkörperanweisungen|Freiformkurven-/Flächenattribute
---|---|---|
|p|Punkt|parm|Parameterwerte|deg|Grad
|l|Linie|trimm|Äußere Trimmschleife|bmat|Basismatrix
|f|Face|Loch|Innere Trimmschlaufe|Stufe|Stufengröße
|curv|Kurve|scrv|Spezielle Kurve|cstype|Kurven- oder Flächentyp
|curv2|2D-Kurve|sp|Spezieller Punkt|**Verbindung und Gruppierung von Flächen**
|surf|Surface|end|Ende-Anweisung|con|connect
|**Attribute anzeigen/darstellen**|g|Gruppenname
|bevel|Abschrägungsinterpolation|shadow_obj|Schattenwurf|s|Glättungsgruppe
|lod|Detaillierungsgrad|trace_obj|Raytracing|mg|Gruppe zusammenführen
|d_interp|Interpolation auflösen|ctech|Kurvennäherungsverfahren|o|Objektname
|c_interp|Farbinterpolation|stech|Oberflächennäherungsverfahren|
|usemtl|Materialname|mtllib|Materialbibliothek|
|**Geometrische Scheitelpunkte**|
|v|Geometrische Eckpunkte|vn|Vertex-Normalen|
|vt|Textureckpunkte|vp|Parameterraumeckpunkte|

### Farbe und Textur

Mit der OBJ-Datei können Farb- und Texturinformationen in einem zugehörigen Dateiformat namens Material Template Library (MTL) gespeichert werden. Mehrfarbige geometrische Modelle werden mit diesen beiden Dateien zusammen gerendert. MTL-Dateien sind ASCII-basiert und erleichtern das Computer-Rendering, indem sie die lichtreflektierenden Eigenschaften einer Oberfläche mithilfe des Modells der Phong-Reflexion beschreiben. Der Standard wurde von einer großen Anzahl von Softwareanbietern übernommen, die seinen Vorteil für den Austausch von Materialien nutzen. Das MTL-Format ist etwas veraltet, da es die neuesten Technologien wie Specular- und Parallax-Maps nicht unterstützt.

## Verweise

* [Wavefront .obj-Datei](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

