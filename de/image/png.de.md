{
  "date" : "2019-10-11",
  "keywords" :[ "png-Datei", "png-Dateiformat", "was ist eine png-Datei", "Datei", "png-Beispiel", "png-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG-Dateiformat - Rasterbilddatei",
  "description":"Erfahren Sie mehr über das PNG-Dateiformat und APIs, die PNG-Dateien erstellen und öffnen können.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PNG-Datei?

Eine **PNG**-Datei (Portable Network Graphics) ist ein Rasterbild-Dateiformat, das verlustfreie Komprimierung verwendet. Dieses Dateiformat wurde als Ersatz für das Graphics Interchange Format ([GIF](/de/image/gif/)) erstellt und unterliegt keinen Urheberrechtsbeschränkungen. Das PNG-Dateiformat unterstützt jedoch keine Animationen. Das PNG-Dateiformat unterstützt die verlustfreie Bildkomprimierung, was es bei seinen Benutzern beliebt macht. Im Laufe der Zeit hat sich PNG zu einem der weit verbreiteten Bilddateiformate entwickelt.

## Kurze Geschichte des PNG-Dateiformats

Der Hauptgrund für die Erstellung des PNG-Dateiformats war der patentierte Komprimierungsalgorithmus Lempel-Ziv-Welch, der im GIF-Dateiformat verwendet wird. Dies führte zusammen mit anderen GIF-Einschränkungen dazu, dass das Dateiformat [**GIF**](/de/image/gif/) ersetzt werden musste. Der erste Vorschlag und Name für das PNG-Dateiformat kam im Januar 1995. Wichtige Ereignisse in Bezug auf PNG-Dateiformate sind unten aufgeführt:

* Oktober 1996: PNG-Spezifikationen Version 1.0 wurden veröffentlicht und erschienen später als [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Dieselben wurden im Oktober 1996 zu einer W3C-Empfehlung.
* Dezember 1998: Version 1.1 wurde mit einigen kleinen Änderungen und dem Hinzufügen von drei neuen Chunks veröffentlicht.
* August 1999: Version 1.2, die einen zusätzlichen Chunk hinzufügt, wurde veröffentlicht.
* November 2003: PNG wurde ein internationaler Standard (ISO/IEC 15948:2003). Diese Version von PNG unterscheidet sich nur geringfügig von Version 1.2 und fügt keine neuen Chunks hinzu.
* März 2004: ISO/IEC 15948:2004

## Funktionsvergleich von GIF und PNG

Das PNG-Dateiformat wurde so konzipiert, dass es einfach und portabel, rechtlich unbelastet, austauschbar, flexibel und robust ist. Die folgende Tabelle listet die GIF-Features auf, die zusätzlich zu den neuen Features vom PNG-Dateiformat geerbt werden.

|Feature|GIF|PNG|
---|---|---|
|Indexfarbenbilder mit bis zu 256 Farben|Ja|Ja|
|Unterstützung für Streaming|Ja|Ja|
|Transparenz|Ja|Ja|
|Zusätzliche Informationen|Ja|Ja|
|Hardware- und Plattformunabhängigkeit|Ja|Ja|
|Wirksam|Ja|Ja|
|Truecolor-Bilder mit bis zu 48 Bit pro Pixel|Nein|Ja|
|Graustufenbilder mit bis zu 16 Bit pro Pixel|Nein|Ja|
|Vollständiger Alphakanal (allgemeine Transparenzmasken)|Nein|Ja|
|Bild-Gammainformationen|Nein|Ja|
|Zuverlässigkeit|Nein|Ja|
|Schnellere Erstpräsentation|Nein|Ja|

## PNG-Dateistruktur

Fast alle Betriebssysteme unterstützen das Öffnen von PNG-Dateien. Zum Beispiel hat der Microsoft Windows-Viewer die Fähigkeit, PNG-Dateien zu öffnen, da das Betriebssystem standardmäßig die Unterstützung bietet, die als Teil der Installation verfügbar ist. Eine PNG-Datei besteht aus einer PNG-„Signatur“, gefolgt von einer Reihe von //Blöcken//.

### Kopfzeile der PNG-Datei

Die ersten acht Bytes einer PNG-Datei enthalten immer die folgenden (dezimalen) Werte:

{{{137 80 78 71 13 10 26 10 }}}

Diese Signatur gibt an, dass der Rest der Datei ein einzelnes PNG-Bild enthält, das aus einer Reihe von Chunks besteht, die mit einem IHDR-Chunk beginnen und mit einem IEND-Chunk enden.

### Brocken ###

Jeder Chunk besteht aus vier Teilen:

**Länge:** Eine 4-Byte-Ganzzahl ohne Vorzeichen, die die Anzahl der Bytes im Datenfeld des Chunks angibt. Die Länge zählt nur das Datenfeld, nicht sich selbst, den Chunk-Typ-Code oder den CRC. Null ist eine gültige Länge. Obwohl Encoder und Decoder die Länge als vorzeichenlos behandeln sollten, darf ihr Wert 231 Bytes nicht überschreiten.

**Chunk-Typ:** Ein 4-Byte-Chunk-Typ-Code. Zur einfacheren Beschreibung und Untersuchung von PNG-Dateien dürfen Typcodes nur aus ASCII-Großbuchstaben und -Kleinbuchstaben (AZ und az oder 65-90 und 97-122 dezimal) bestehen. Codierer und Decodierer müssen die Codes jedoch als feste Binärwerte behandeln, nicht als Zeichenfolgen. Beispielsweise wäre es nicht korrekt, den Typencode IDAT durch die EBCDIC-Äquivalente dieser Buchstaben darzustellen. Weitere Namenskonventionen für Chunk-Typen werden im nächsten Abschnitt erläutert.

**Chunk-Daten:** Die dem Chunk-Typ entsprechenden Datenbytes, falls vorhanden. Dieses Feld kann die Länge Null haben.

**CRC:** Ein 4-Byte-CRC (Cyclic Redundancy Check), der anhand der vorhergehenden Bytes im Chunk berechnet wird, einschließlich des Chunk-Typcodes und der Chunk-Datenfelder, aber ohne das Längenfeld. Der CRC ist immer vorhanden, sogar für Chunks, die keine Daten enthalten.

Die Chunk-Datenlänge kann eine beliebige Anzahl von Bytes bis zum Maximum sein; Daher können Implementierer nicht davon ausgehen, dass Chunks an Grenzen ausgerichtet sind, die größer als Bytes sind.

Chunks können in beliebiger Reihenfolge erscheinen, vorbehaltlich der Beschränkungen für jeden Chunk-Typ. (Eine bemerkenswerte Einschränkung ist, dass IHDR zuerst erscheinen muss und IEND zuletzt erscheinen muss; somit dient der IEND-Chunk als End-of-File-Marker.) Mehrere Chunks des gleichen Typs können erscheinen, aber nur, wenn dies ausdrücklich für diesen Typ erlaubt ist.

#### Chunk-Typen

Die Chunk-Typen werden basierend auf dem dem Chunk-Typ zugewiesenen 4-Byte-ASCII-Wert mit Berücksichtigung der Groß- und Kleinschreibung in **Kritische** und **Ergänzende** Chunks kategorisiert. Alle Implementierungen müssen die standardmäßigen kritischen Chunks verstehen und erfolgreich rendern. Ein gültiges PNG-Bild muss einen IHDR-Blöcke, einen oder mehrere IDAT-Blöcke und einen IEND-Blöcke enthalten.

### Kompression

Die PNG-Komprimierungsmethode 0 (die einzige derzeit für PNG definierte Komprimierungsmethode) spezifiziert die Deflate/Inflate-Komprimierung mit einem gleitenden Fenster von höchstens 32768 Bytes. Deflate-Komprimierung ist ein LZ77-Derivat, das in zip, gzip, pkzip und verwandten Programmen verwendet wird. Umfangreiche Untersuchungen wurden durchgeführt, um seinen patentfreien Status zu unterstützen. Die komprimierten Daten innerhalb des zlib-Datenstroms werden als eine Reihe von Blöcken gespeichert, von denen jeder rohe (unkomprimierte) Daten, LZ77-komprimierte Daten, die mit festen Huffman-Codes codiert sind, oder LZ77-komprimierte Daten, die mit benutzerdefinierten Huffman-Codes codiert sind, darstellen kann. Ein Markierungsbit im letzten Block identifiziert ihn als letzten Block, wodurch der Decoder das Ende des komprimierten Datenstroms erkennen kann.

#### Filterung vor der Komprimierung

Vorkomprimierungsfilter werden angewendet, um die Bilddaten für eine optimale Komprimierung vorzubereiten. Die PNG-Filtermethode definiert fünf grundlegende Filtertypen wie folgt:

|Filtertyp|Name|Vorhergesagter Wert|
---|---|---|
|0|Keine|Die Scanline wird unverändert übertragen|
|1|Sub|Überträgt die Differenz zwischen jedem Byte und dem Wert des entsprechenden Bytes des vorherigen Pixels.|
|2|Up|Der Up()-Filter ist genau wie der Sub()-Filter, außer dass das Pixel direkt über dem aktuellen Pixel und nicht nur links davon als Prädiktor verwendet wird.|
|3|Average|Der Filter Average() verwendet den Durchschnitt der beiden benachbarten Pixel (links und oben), um den Wert eines Pixels vorherzusagen.|
|4|Paeth|Der Paeth()-Filter berechnet eine einfache lineare Funktion der drei benachbarten Pixel (links, oben, oben links) und wählt dann als Prädiktor das benachbarte Pixel, das dem berechneten Wert am nächsten ist.|

Filteralgorithmen werden auf "Bytes" angewendet, nicht auf Pixel, unabhängig von der Bittiefe oder dem Farbtyp des Bildes. Die Filteralgorithmen arbeiten an der Bytefolge, die durch eine Scanline gebildet wird. Wenn das Bild einen Alphakanal enthält, werden die Alphadaten auf die gleiche Weise wie die Bilddaten gefiltert.

Wenn das Bild interlaced ist, wird jeder Durchgang des Interlace-Musters zu Filterzwecken als unabhängiges Bild behandelt. Die Filter arbeiten mit den Byte-Folgen, die durch die tatsächlich während eines Durchlaufs übertragenen Pixel gebildet werden, und die "vorherige Abtastzeile" ist diejenige, die zuvor in demselben Durchlauf übertragen wurde, nicht diejenige, die im vollständigen Bild benachbart ist. Beachten Sie, dass das in einem Durchlauf übertragene Teilbild immer rechteckig ist, aber eine geringere Breite und/oder Höhe als das vollständige Bild hat. Die Filterung wird nicht angewendet, wenn dieses Unterbild leer ist.

## Verweise ##

* [PNG - Startseite](http://www.libpng.org/pub/png/)

