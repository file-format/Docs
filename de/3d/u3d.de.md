{
  "date" : "2019-10-11",
  "keywords" :[ "u3d-Datei", "u3d-Dateiformat", "was ist eine u3d-Datei", "Datei", "u3d-Beispiel", "u3d-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Universelles 3D-Dateiformat",
  "description":"Erfahren Sie mehr über das U3D-Dateiformat und APIs, die U3D-Dateien öffnen und erstellen können.",
  "linktitle" :"U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine U3D-Datei?

**U3D** (Universal 3D) ist ein komprimiertes Dateiformat und eine Datenstruktur für 3D-Computergrafik. Es enthält 3D-Modellinformationen wie Dreiecksnetze, Beleuchtung, Schattierung, Bewegungsdaten, Linien und Punkte mit Farbe und Struktur. Das Format wurde im August 2005 als [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm) Standard akzeptiert. 3D [PDF](/de/pdf/) Dokumente unterstützen U3D Objekte einbetten und können in Adobe Reader (Version 7 und höher) angezeigt werden. Das U3D-Format wurde mit dem Ziel entwickelt, einen universellen Standard für die Speicherung und den Austausch von dreidimensionalen Daten zu etablieren. Das Format findet jedoch seine Hauptanwendung in der Codierung für 3D-PDF und nicht als Austauschformat. Acrobat 3D konvertiert einen unterstützten 3D-Dateityp bei der Konvertierung in das PDF entweder in U3D oder PRC.

## U3D-Dateiformat

U3D-Dateien liegen im binären Dateiformat vor, das vier Editionen unterzogen wurde, wie im Referenzdokument [ECMA-363] (http://www.ecma-international.org/publications/standards/Ecma-363.htm) beschrieben, was zu einer Aktualisierung der Spezifikationen führte mit jeder Ausgabe. Der PDF-Dateistandard ISO-32000 akzeptiert U3D als zulässigen Annotations- und Multimediatyp.

Die erste Ausgabe von U3D konzentrierte sich auf die wichtigsten Darstellungen von 3D-Grafikeigenschaften wie Geometrie, Farbe, Texturen, Beleuchtung, Knochen und transformbasierte Animation. Die zweite und dritte Ausgabe korrigierten einige Errata in der ersten Ausgabe, wobei die dritte Version der am häufigsten verwendete Typ in der Industriesoftware ist. Die vierte Ausgabe enthält Definitionen für Grundelemente höherer Ordnung (gekrümmte Oberflächen). [U3D-Spezifikationen] (http://www.ecma-international.org/publications/standards/Ecma-363.htm) sind online als Benutzerreferenz auf der ECMA-Website verfügbar.

### Datentypen in U3D-Dateien

Die Binärdatei enthält die folgenden Typen: U8, U16, U32, U64, I16, I32, F32, F64 und String.

* U8 : Eine vorzeichenlose 8-Bit-Ganzzahl
* U16 : Eine vorzeichenlose 16-Bit-Ganzzahl
* U32 : Eine vorzeichenlose 32-Bit-Ganzzahl
* U64 : Eine vorzeichenlose 64-Bit-Ganzzahl
* I16 : Eine vorzeichenbehaftete 16-Bit-Ganzzahl
* F32: Ein IEEE-Float mit einfacher Genauigkeit.
* F64: Ein IEEE-Float mit doppelter Genauigkeit.
* Zeichenfolge: Zeichenfolgen in einer U3D-Datei beginnen mit einer vorzeichenlosen 16-Bit-Ganzzahl, die die Gesamtlänge der Zeichen in der Zeichenfolge definiert. Bei Strings wird immer zwischen Groß- und Kleinschreibung unterschieden.

## U3D-Dateistruktur

Eine U3D-Datei enthält eine Folge von Blöcken. In jeder U3D-Datei gibt es 3 verschiedene Arten von Blöcken.

* Datei-Header-Block
* Deklarationsblock
* Fortsetzungsblock

Der Lader bestimmt das Ende eines Blocks, wenn die Daten in diesem Block nicht erforderlich sind oder wenn ein Decoder für diesen Blocktyp nicht verfügbar ist.

{{< figure src="../u3d.png" alt="U3D-Dateiformat" >}}

### Datei-Header-Block
Ein Dateikopfblock enthält Dateiinformationen, die vom geladenen verwendet werden, um zu bestimmen, wie die Datei zu lesen ist.

### Deklarationsblock

Die Deklarationsblöcke enthalten Informationen über die Objekte in der Datei. Die Objekte in einem Deklarationsblock müssen definiert werden.

### Fortsetzungsblock

Zusätzliche Informationen für in einem Deklarationsblock deklarierte Objekte werden im Fortsetzungsblock bereitgestellt. Jeder Fortsetzungsblock muss einem Deklarationsblock zugeordnet werden.


## Verweise ##

* [U3D-Dateiformat – Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D-Dateiformatspezifikationen](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

