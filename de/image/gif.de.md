{
  "date" : "2019-10-11",
  "keywords" :[ "gif-Datei", "gif-Dateiformat", "was ist eine gif-Datei", "Datei", "gif-Beispiel", "gif-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Bilddateiformat",
  "description":"Erfahren Sie mehr über das GIF-Dateiformat und APIs, die GIF-Dateien erstellen und öffnen können.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GIF-Datei? ##

Ein GIF oder Graphical Interchange Format ist eine Art stark komprimiertes Bild. GIF gehört Unisys und verwendet den LZW-Komprimierungsalgorithmus, der die Bildqualität nicht beeinträchtigt. Für jedes Bild sind in GIF normalerweise bis zu 8 Bit pro Pixel und bis zu 256 Farben im gesamten Bild zulässig. Im Gegensatz zu einem [JPEG](/de/image/jpeg/)-Bild, das bis zu 16 Millionen Farben darstellen kann und ziemlich an die Grenzen des menschlichen Auges stößt. Als das Internet aufkam, blieben GIFs die beste Wahl, da sie eine geringe Bandbreite erforderten und für die Grafiken kompatibel waren, die Volltonbereiche verbrauchen. Ein animiertes GIF kombiniert zahlreiche Bilder oder Frames in einer einzigen Datei und zeigt sie in einer Sequenz an, um einen animierten Clip oder ein kurzes Video zu erstellen. Die Farbbeschränkungen betragen bis zu 256 für jedes Bild und sind wahrscheinlich am wenigsten geeignet, um andere Bilder und Fotos mit Farbverlauf zu reproduzieren.

## GIF-Dateiformat ##

Konzeptionell haben GIF-Dateien einen grafischen Bereich mit fester Größe, der mit null oder mehr Bildern gefüllt ist. Einige GIF-Dateien unterteilen den grafischen Bereich oder Blöcke mit fester Größe in Unterbilder, die im Fall von animierten GIFs als animierte Frames fungieren können. Das GIF-Format verwendet Pixeltiefen von 1 bis 8 Bit, um die Bitmap-Daten zu speichern. RGB-Farbmodell- und Palettendaten werden immer verwendet, um die Bilder zu speichern. Je nach Version definiert ein Header fester Länge ("GIF87a" oder "GIF89a") den Beginn einer typischen GIF-Datei.

Derzeit sind zwei Versionen von GIF verfügbar: 87a und 89a. Ersteres ist das ursprüngliche GIF-Format, während letzteres das neue GIF-Format ist. In diesem Dateiformat werden die Eigenschaften der Blöcke und Pixelabmessungen in einem logischen Bildschirmdeskriptor fester Länge erwähnt. Das Vorhandensein und die Größe einer globalen Farbtabelle kann durch den Bildschirmdeskriptor spezifiziert werden, der weitere Details verfolgt, falls vorhanden. Der Trailer ist das letzte Byte der Datei, das ein einzelnes Byte eines ASCII-Semikolons enthält. Ein typisches GIF87a-Dateilayout sieht wie folgt aus:

### Header ###

Der Header enthält sechs Bytes und wird verwendet, um den Dateityp als GIF anzugeben. Obwohl der Logical Screen Descriptor vom eigentlichen Header getrennt ist, wird er manchmal als zweiter Header betrachtet. Dieselbe Struktur, die zum Speichern des Headers verwendet wird, kann den Logical Screen Descriptor speichern. Alle GIF-Dateien beginnen mit der 3-Byte-Signatur und verwenden die Zeichen „GIF“ als Kennung. Die Version ist ebenfalls drei Bytes groß und gibt die Version der GIF-Datei an.

### Logischer Bildschirmdeskriptor ###

Ein Bilddeskriptor fester Länge gibt die Bildschirm- und Farbinformationen an, die zum Erstellen des GIF-Bildes erforderlich sind. Die Felder Höhe und Breite umfassen den kleinsten Wert der Bildschirmauflösung, der für die Anzeige der Bilddaten obligatorisch ist. Wenn das Anzeigegerät nicht in der Lage ist, die angegebene Auflösung anzuzeigen, ist eine Skalierung erforderlich, um das Bild angemessen anzuzeigen. Bildschirm- und Farbabbildungsinformationen werden von den vier Unterfeldern der folgenden Tabelle angezeigt (wobei Bit 0 das niederwertigste Bit ist):


|Bits|Unterfelder
---|---|
|0-2|Größe der globalen Farbtabelle
|3|Farbtabellen-Sortierkennzeichen
|4-6|Farbauflösung
|7|Globale Farbtabellenflagge

#### Globale Farbtabelle ####

Eine optionale globale Farbtabelle wird direkt nach dem logischen Bildschirmdeskriptor platziert. Diese Tabelle wird abgebildet, um die Pixelfarbdaten innerhalb der Bilddaten zu indizieren. In Ermangelung einer globalen Farbtabelle verwendet jedes Bild in der GIF-Datei seine lokale Farbe. Es ist besser, eine Standardfarbtabelle bereitzustellen, wenn sowohl die globale als auch die lokale Farbtabelle fehlen. Eine Reihe von Drei-Byte-Tripeln setzt die Elemente der Farbtabelle zusammen. Jedes Byte charakterisiert einen RGB-Farbwert. Die Farben Rot, Grün und Blau werden als Werte jedes Farbtabellenelements verwendet. Die Einträge in der globalen Farbtabelle umfassen maximal 256 Einträge und repräsentieren immer eine Zweierpotenz.

#### Bilddaten ####

Die Bilddaten speichern ein Byte von uncodierten Symbolen, gefolgt von einer verketteten Liste von Teilzeichen zusammen mit den LZW-codierten Daten.

#### Anhänger ####

Trailer stellt ein einzelnes Datenbyte dar, das das letzte Zeichen in der Datei ist. Der Wert dieses Bytes ist fest 3Bh und gibt das Ende des Datenstroms an. Jede GIF-Datei muss den Trailer am Ende jeder Datei haben.

## Verweise ##

* [GIF-Dateiformat](https://en.wikipedia.org/wiki/GIF)

