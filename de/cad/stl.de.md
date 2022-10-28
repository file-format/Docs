{
  "date" : "2020-03-16",
  "keywords" :[ "STL-Datei", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das STL-Dateiformat und APIs, die STL-Dateien erstellen und öffnen können.",
  "title" :"STL-Dateiformat",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine STL-Datei?

STL, Abkürzung für Stereolithrographie, ist ein austauschbares Dateiformat, das dreidimensionale Oberflächengeometrie darstellt. Das Dateiformat findet seine Verwendung in verschiedenen Bereichen wie Rapid Prototyping, 3D-Druck und computergestützter Fertigung. Es stellt eine Oberfläche als eine Reihe kleiner Dreiecke dar, die als Facetten bekannt sind, wobei jede Facette durch eine senkrechte Richtung und drei Punkte beschrieben wird, die die Eckpunkte des Dreiecks darstellen. Die resultierenden Daten werden von Anwendungen verwendet, um den Querschnitt der 3D-Form zu bestimmen, die vom Hersteller gebaut werden soll. Im STL-Dateiformat sind keine Informationen zur Darstellung von Farbe, Textur oder anderen gängigen [CAD](/de/cad/)-Modellattributen verfügbar.

## Kurze Geschichte ##

Die Entwicklung des STL-Dateiformats geht auf das Jahr 1987 zurück. Es wurde von 3D Systems für die Verwendung in kommerziellen 3D-Druckern entwickelt. Eine überarbeitete Version des STL-Dateiformats, bekannt als STL 2.0, wurde 2009 mit Aktualisierungen des Dateiformats vorgeschlagen.

## Dateiformatspezifikationen ##

Eine STL-Datei repräsentiert eine Oberflächengeometrie mit Facetten. Die Facetten definieren die Oberfläche eines 3D-Objekts und werden durch eine Einheitsnormale, die eine senkrecht zum Dreieck verlaufende Linie mit einer Länge von 1,0 ist, und durch drei Eckpunkte eindeutig identifiziert. Es sind insgesamt 12 Zahlen für jede Facette als Normale gespeichert und jeder Scheitelpunkt wird durch jeweils drei Koordinaten angegeben. Die StL-Datei enthält keine Skaleninformationen; die Koordinaten sind in willkürlichen Einheiten.

Die Spezifikationen des STL-Dateiformats können unter folgenden zwei Aspekten untersucht werden.

### Facettenorientierung ###

Die Ausrichtung einer Facette wird durch die Richtung der Einheitsnormalen und die Reihenfolge bestimmt, in der die Scheitelpunkte aufgelistet sind. Die Ausrichtung der Facetten wird auf zwei Arten wie folgt angegeben:

* Die Richtung der Normalen ist nach außen
* Die Scheitelpunkte werden von außen gegen den Uhrzeigersinn aufgelistet, wobei die Regel der rechten Hand eingehalten wird.

### Scheitelpunkt-zu-Scheitelpunkt-Regel ###

Gemäß dieser Regel teilt jedes Dreieck zwei Eckpunkte mit jedem seiner benachbarten Dreiecke. Somit kann ein Eckpunkt eines Dreiecks nicht auf der Seite eines anderen Dreiecks liegen.

## Dateiformate ##

STL ist sowohl in ASCII- als auch in binären Darstellungen für ein kompaktes Dateiformat verfügbar.

### STL-ASCII-Format ###

Die ASCII-Version des STL-Dateiformats ist in reinem ASCII geschrieben. Aufgrund seiner Größe wird das Dateiformat jedoch nicht als bevorzugtes Format für die Verwendung ausgewählt. Die Syntax einer ASCII-STL-Datei lautet wie folgt:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Die fettgedruckten Wörter stellen Schlüsselwörter dar, die immer in Kleinbuchstaben geschrieben werden sollten. Kursive Symbole sind Variablen, die durch benutzerdefinierte Werte ersetzt werden sollen. Die numerischen Daten in den Linien **facet normal** und **vertex** sind Gleitkommazahlen mit einfacher Genauigkeit, z. B. 1,23456E+789. Eine **Facettennormal**-Koordinate kann ein führendes Minuszeichen haben; eine **Scheitelpunkt**-Koordinate möglicherweise nicht.

### STL-Binärformat ###

Das Binärformat verwendet die numerische Darstellung von IEEE-Ganzzahlen und Fließkommazahlen. Das Dateiformat wird wie folgt dargestellt:

|Feld|Info|
---|---|
|Kopfzeile|80 Zeichen|
|Anzahl der Dreiecke|4-Byte-Little-Endian-Ganzzahl ohne Vorzeichen|
|Daten für jedes Dreieck|12 32-Bit-Gleitkommazahlen|

Eine ausführlichere Ansicht des Dateiformats ist unten dargestellt.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Verweise ##

* [Das STL-Format](http://www.fabbers.com/tech/STL_Format)
* [STL - von Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

