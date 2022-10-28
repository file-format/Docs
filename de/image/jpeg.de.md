{
  "date" : "2019-11-25",
  "keywords" :[ "jpeg-Datei", "jpeg-Dateiformat", "was ist eine jpeg-Datei", "Datei", "jpeg-Beispiel", "jpeg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Bilddateiformat",
  "description":"Erfahren Sie mehr über das JPEG-Dateiformat und APIs, die JPEG-Dateien erstellen und öffnen können.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Was ist eine JPEG-Datei? ##

Ein JPEG ist ein Bildformat, das mit der Methode der verlustbehafteten Komprimierung gespeichert wird. Das Ausgabebild ist als Ergebnis der Komprimierung ein Kompromiss zwischen Speichergröße und Bildqualität. Benutzer können die Komprimierungsstufe anpassen, um die gewünschte Qualitätsstufe zu erreichen, während gleichzeitig die Speichergröße reduziert wird. Die Bildqualität wird vernachlässigbar beeinträchtigt, wenn eine 10:1-Komprimierung auf das Bild angewendet wird. Je höher der Komprimierungswert, desto stärker die Verschlechterung der Bildqualität.

## Dateiformatspezifikationen ##

Das JPEG-Bilddateiformat wurde von der Joint Photographic Experts Group standardisiert, daher der Name JPEG. Das Format war die Wahl zum Speichern und Übertragen von fotografischen Bildern im Internet. Fast alle Betriebssysteme haben jetzt Viewer, die die Visualisierung von JPEG-Bildern unterstützen, die oft auch mit der JPG-Erweiterung gespeichert werden. Sogar die Webbrowser unterstützen die Visualisierung von JPEG-Bildern. Bevor auf die Spezifikationen des JPEG-Dateiformats eingegangen wird, muss der Gesamtprozess der Schritte zur JPEG-Erstellung erwähnt werden.

### JPEG-Komprimierungsschritte ###

**Transformation:** Farbbilder werden von RGB in ein Luminanz-/Chrominanzbild umgewandelt (das Auge reagiert empfindlich auf Luminanz, nicht auf Chrominanz, sodass der Chrominanzteil viele Daten verlieren und daher stark komprimiert werden kann.

**Downsampling:** Das Downsampling wird für die Farbkomponente und nicht für die Luminanzkomponente durchgeführt. Das Downsampling erfolgt entweder im Verhältnis 2:1 horizontal und 1:1 vertikal (2h 1 V). Da die 'y'-Komponente nicht berührt wird, verringert sich die Größe des Bildes, es gibt keinen merklichen Verlust an Bildqualität.

**Organisieren in Gruppen:** Die Pixel jeder Farbkomponente sind in Gruppen von 8×2 Pixeln organisiert, die als „Dateneinheiten“ bezeichnet werden. Wenn die Anzahl der Zeilen oder Spalten kein Vielfaches von 8 ist, werden die unterste Zeile und die Spalten ganz rechts dupliziert.

**Diskrete Cosinus-Transformation:** Diskrete Cosinus-Transformation (DCT) wird dann auf jede Dateneinheit angewendet, um eine 8×8-Karte der transformierten Komponenten zu erstellen. Aufgrund der begrenzten Genauigkeit der Computerarithmetik geht bei der DCT ein gewisser Informationsverlust einher. Das bedeutet, dass es auch ohne die Karte zu einem gewissen Verlust an Bildqualität kommt, der jedoch normalerweise gering ist.

**Quantisierung:** Jede der 64 transformierten Komponenten in der Dateneinheit wird durch eine separate Zahl namens „Quantisierungskoeffizient (QC)“ dividiert und dann auf eine ganze Zahl gerundet. Hier gehen Informationen unwiederbringlich verloren, große QC verursachen mehr Verlust. Im Allgemeinen erlauben die meisten JPEG-Implementierungen die Verwendung von QC-Tabellen, die vom JPEG-Standard empfohlen werden.

**Codierung:** Die 64 quantisierten transformierten Koeffizienten (die nun ganze Zahlen sind) jeder Dateneinheit werden unter Verwendung einer Kombination aus RLE- und Huffman-Codierung codiert.

**Header hinzufügen:** Der letzte Schritt fügt Header und alle verwendeten JPEG-Parameter hinzu und gibt das Ergebnis aus.

Der JPEG-Decoder verwendet die Schritte in umgekehrter Reihenfolge, um aus dem komprimierten das Originalbild zu erzeugen.

### Dateistruktur ###

Ein JPEG-Bild wird als Sequenz von Segmenten dargestellt, wobei jedes Segment mit einer Markierung beginnt. Jeder Marker beginnt mit einem 0xFF-Byte, gefolgt von einem Marker-Flag, um den Typ des Markers darzustellen. Die Nutzlast, gefolgt von der Markierung, ist je nach Markierungstyp unterschiedlich. Gängige JPEG-Markierungstypen sind unten aufgeführt:

|Kurzname|Bytes|Nutzlast|Name|Kommentare
---|---|---|---|---|
|SOI|0xFF, 0xD8|keine|Bildanfang|
|S0F0|0xFF, 0xC0|variable Größe|Beginn des Frames|
|S0F2|0xFF, 0xC2|variable Größe|Start für Frame|
|DHT|0xFF, 0xC4|variable Größe|Huffman-Tabellen definieren|
|DQT|0xFF, 0xDB|variable Größe|Definiere Quantisierungstabelle(n)|
|DRI|0xFF, 0xDD|4 Bytes|Neustartintervall definieren|
|SOS|0xFF, 0xDA|variable Größe|Scanbeginn|
|RSTn|0xFF, 0xD//n//(/de//n//#0..7)|keine|Neustart|
|APPn|0xFF, 0xE//n//|variable Größe|Anwendungsspezifisch|
|COM|0xFF, 0xFE|variable Größe|Kommentar|
|EOI|0xFF, 0xD9|keine|Bildende|

Innerhalb der entropiecodierten Daten wird nach jedem 0xFF-Byte ein 0x00-Byte vom Encoder vor dem nächsten Byte eingefügt, so dass dort keine Markierung zu sein scheint, wo keine beabsichtigt ist, wodurch Framing-Fehler verhindert werden. Decoder müssen dieses 0x00-Byte überspringen. Diese Technik namens [Byte Stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (siehe Abschnitt F.1.2.3 der JPEG-Spezifikation) wird nur auf die entropiecodierten Daten angewendet, nicht auf die Nutzlastdaten . Beachten Sie jedoch, dass entropiecodierte Daten einige eigene Markierungen haben; insbesondere die Reset-Marker (0xD0 bis 0xD7), die verwendet werden, um unabhängige Blöcke entropiecodierter Daten zu isolieren, um eine parallele Decodierung zu ermöglichen, und Encoder können diese Reset-Marker in regelmäßigen Abständen einfügen (obwohl nicht alle Encoder dies tun).

