{
  "date" : "2019-10-11",
  "keywords" :[ "tiff-Datei", "tiff-Dateiformat", "was ist eine tiff-Datei", "Datei", "tiff-Beispiel", "tiff-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Bilddateiformat",
  "description":"Erfahren Sie mehr über das TIFF-Dateiformat und APIs, die TIFF-Dateien erstellen und öffnen können.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine TIFF-Datei?

TIFF oder TIF, Tagged Image File Format, stellt Rasterbilder dar, die für die Verwendung auf einer Vielzahl von Geräten gedacht sind, die diesem Dateiformatstandard entsprechen. Es ist in der Lage, Bilevel-, Graustufen-, Palettenfarben- und Vollfarben-Bilddaten in mehreren Farbräumen zu beschreiben. Es unterstützt sowohl verlustbehaftete als auch verlustfreie Komprimierungsschemata, um zwischen Speicherplatz und Zeit für Anwendungen zu wählen, die das Format verwenden. Das Format ist nicht maschinenabhängig und frei von Grenzen wie Prozessor, Betriebssystem oder Dateisystem.

## Kurze Geschichte des TIFF-Dateiformats

Das TIFF-Dateiformat wurde ursprünglich im Herbst 1986 von der Aldus Corporation nach einer Reihe von Treffen mit verschiedenen Scannerherstellern und Softwareentwicklern erstellt. Der Hauptzweck des TIFF-Dateiformats bestand darin, allen Anbietern von Desktop-Scannern ein gemeinsames Dateiformat für gescannte Bilder bereitzustellen. Beginnend mit der Unterstützung nur des binären Bildformats entwickelte sich das Format im Laufe der Zeit zur Unterstützung von Graustufen- und Farbbildern. Die ursprüngliche Version der TIFF-Dateiformatspezifikationen kann als Revision 3.0 bezeichnet werden, da es zwei frühere Entwurfsversionen gab. Eine Hauptversion 5.0 wurde 1988 veröffentlicht, die Unterstützung für Palettenfarbbilder und LZW-Komprimierung hinzufügte. Revision 6.0 der TIFF-Dateiformate wurde danach 1992 veröffentlicht. 1994 erwarb Adobe Systems Aldus und die Spezifikationen sind jetzt verfügbar und werden von Adobe Systems gepflegt.

## Spezifikationen des TIFF-Dateiformats

Das TIFF-Dateiformat ist erweiterbar und wurde mehrfach überarbeitet, wodurch eine unbegrenzte Menge an privaten oder speziellen Informationen aufgenommen werden kann. Eine TIFF-Datei beginnt mit einem 8-Byte-Header, wobei die Bytes Zahlen von 0 bis N sind. Die größtmögliche TIFF-Datei hat eine Länge von 2**32 Bytes. Die Datei beginnt mit einem 8-Byte-Bilddatei-Header, der direkt auf eine Bilddatei (IFD) zeigt. Ein IFD enthält Informationen über das Bild sowie Verweise auf die eigentlichen Bilddaten.

### Kopfzeile der TIFF-Datei

Der 8-Byte-Header der TIFF-Datei enthält die folgenden Informationen:

**Bytes 0-1:** Die in der Datei verwendete Byte-Reihenfolge. Zulässige Werte sind: „II“ (4949.H) „MM“ (4D4D.H).

Im „II“-Format ist die Byte-Reihenfolge sowohl für 16-Bit- als auch für 32-Bit-Ganzzahlen immer vom niederwertigsten Byte zum höchstwertigen Byte. Dies wird als Little-Endian-Byte-Reihenfolge bezeichnet. Im „MM“-Format ist die Byte-Reihenfolge sowohl für 16-Bit- als auch für 32-Bit-Ganzzahlen immer von der höchstwertigen zur niederwertigsten. Dies wird Big-Endian-Byte-Reihenfolge genannt.

**Bytes 2-3:** Eine willkürliche, aber sorgfältig gewählte Zahl (42), die die Datei weiter als TIFF-Datei identifiziert. Die Byte-Reihenfolge hängt vom Wert der Bytes 0-1 ab.

**Bytes 4-7:** Der Offset (in Bytes) des ersten IFD. Das Verzeichnis kann sich an einer beliebigen Stelle in der Datei nach dem Header befinden, muss jedoch an einer Wortgrenze beginnen. Insbesondere kann ein Bilddateiverzeichnis den Bilddaten folgen, die es beschreibt. Leser müssen den Zeigern folgen, wo immer sie hinführen. Der Begriff Byte-Offset wird in diesem Dokument immer verwendet, um sich auf eine Position in Bezug auf den Anfang der TIFF-Datei zu beziehen. Das erste Byte der Datei hat einen Offset von 0.

### Bilddateiverzeichnis

Ein IFD enthält Informationen über das Bild sowie Zeiger auf die eigentlichen Bilddaten. Es besteht aus einer 2-Byte-Zählung der Anzahl von Verzeichniseinträgen (dh der Anzahl von Feldern), gefolgt von einer Folge von 12-Byte-Feldeinträgen , gefolgt von einem 4-Byte-Offset des nächsten IFD (oder 0, wenn keine). Es muss mindestens 1 IFD in einer TIFF-Datei vorhanden sein und jedes IFD muss mindestens einen Eintrag haben.

#### IFD-Eintrag

Jeder 12-Byte-IFD-Eintrag hat das folgende Format.


|Bytes|Beschreibung
---|---|
|0-1|Das Tag, das das Feld identifiziert
|2-3|Der Feldtyp
|4-7|Zählung des angegebenen Typs
|8-11|Der Wert-Offset, der Datei-Offset (in Bytes) des Werts für das Feld. Der Wert soll an einer Wortgrenze beginnen; der entsprechende Value Offset ist somit eine gerade Zahl. Dieser Dateiversatz kann überall in der Datei zeigen, sogar nach den Bilddaten

Ein TIFF-Feld ist eine logische Einheit, die aus einem TIFF-Tag und seinem Wert besteht. Dieses logische Konzept wird als IFD-Eintrag implementiert, plus der tatsächliche Wert, falls er nicht in den Wert/Offset-Teil passt, die letzten 4 Bytes des IFD-Eintrags. Die Begriffe TIFF-Feld und IFD-Eintrag sind in den meisten Zusammenhängen austauschbar.

### Baseline-TIFF ###

Baseline TIFF ist der Kern von TIFF, das Wesentliche, das alle Mainstream-TIFF-Entwickler in ihren Produkten unterstützen sollten. Die Konformität mit dem TIFF-Format unterliegt der Einhaltung der Baseline-TIFF-Anforderungen. Diese Anforderungen sind im Spezifikationsdokument 6.0 gut dokumentiert.

#### Mehrere Bilder pro Datei ####

Eine TIFF-Datei kann mehr als ein IFD enthalten. Jede IFD definiert eine Unterdatei. Eine mögliche Verwendung von Unterdateien besteht darin, verwandte Bilder zu beschreiben, wie beispielsweise die Seiten einer Faxübertragung. Ein Baseline-TIFF-Lesegerät ist nicht erforderlich, um weitere IFDs nach dem ersten zu lesen.

#### Bildtypen ####

Das Basis-TIFF-Bild hat folgende Typen:

**Bilevel:** Ein Bilevel-Bild enthält zwei Farben – Schwarz und Weiß. TIFF ermöglicht es einer Anwendung, zweistufige Daten entweder in einem Weiß-ist-Null- oder Schwarz-ist-Null-Format auszugeben. Das Feld, das diese Informationen aufzeichnet, heißt **PhotometricInterpretation**.

* RGB-Vollfarbe

Photometrische Interpretationsinformationen für Bilevel-Bilder lauten wie folgt:

Tag = 262 (106.H)
Typ = KURZ
**Werte**

|Wert|Beschreibung|
---|---|
|0|Für Bilevel- und Graustufenbilder: 0 wird als Weiß abgebildet. Der Maximalwert wird schwarz abgebildet. Dies ist der normale Wert für Compression#2|
|1|SchwarzIstNull. Für Bilevel- und Graustufenbilder: 0 wird als Schwarz abgebildet. Der Maximalwert wird weiß abgebildet. Wenn dieser Wert für Komprimierung Nr. 2 angegeben ist, sollte das Bild umgekehrt angezeigt und gedruckt werden.|

**GrayScale:** Graustufenbilder sind eine Verallgemeinerung von Bilevel-Bildern. Bilevel-Bilder können nur Schwarz-Weiß-Bilddaten speichern, aber Graustufenbilder können auch Grauschattierungen speichern. Um solche Bilder zu beschreiben, müssen Sie die folgenden Felder hinzufügen oder ändern. Die anderen Pflichtfelder sind die gleichen wie die für Bilevel-Bilder. Für Graustufenbilder Komprimierung Nr. 1 oder 32773 (PackBits). In Baseline TIFF können Graustufenbilder entweder als unkomprimierte Daten gespeichert oder mit dem PackBits-Algorithmus komprimiert werden.

**BitsPerSample**-Informationen für Graustufenbilder lauten wie folgt:

Tag = 258 (102.H)
Typ = KURZ

Die Anzahl der Bits pro Komponente. Zulässige Werte für Baseline-TIFF-Graustufenbilder sind 4 und 8, was entweder 16 oder 256 unterschiedliche Grauschattierungen zulässt.

**Palette-Color:** Bilder in Palettenfarbe ähneln Graustufenbildern. Sie haben immer noch eine Komponente pro Pixel, aber der Komponentenwert wird als Index in eine vollständige RGB-Nachschlagetabelle verwendet. Um solche Bilder zu beschreiben, müssen Sie die folgenden Felder hinzufügen oder ändern. Die anderen Pflichtfelder sind die gleichen wie bei Graustufenbildern.
Photometrische Interpretationsinformationen für Palette-Color-Bilder lauten wie folgt:

Photometrische Interpretation = 3 (Farbpalette).
ColorMapTag = 320 (140.H)
Typ = KURZ
N = 3 * (2 Bit pro Abtastung)

Dieses Feld definiert eine Rot-Grün-Blau-Farbkarte (oft als Nachschlagetabelle bezeichnet) für Palettenfarbbilder. In einem Palettenfarbbild wird ein Pixelwert verwendet, um in eine RGB-Nachschlagetabelle zu indizieren. Beispielsweise würde ein Farbpalettenpixel mit einem Wert von 0 entsprechend dem 0. Rot-Grün-Blau-Triplett angezeigt. In einer TIFF-ColorMap kommen alle Rotwerte zuerst, gefolgt von den Grünwerten und dann den Blauwerten. In der ColorMap wird Schwarz durch 0,0,0 und Weiß durch 65535, 65535, 65535 dargestellt.

**RGB-Vollfarbe:** In einem RGB-Bild besteht jedes Pixel aus drei Komponenten: Rot, Grün und Blau. Es gibt keine ColorMap. Um ein RGB-Bild zu beschreiben, müssen Sie die folgenden Felder und Werte hinzufügen oder ändern. Die anderen Pflichtfelder sind die gleichen wie die für Palettenfarbenbilder.

Bit pro Abtastung = 8,8,8. Jede Komponente ist in einem Baseline-TIFF-RGB-Bild 8 Bit tief.

PhotometricInterpretation = 2 (RGB) und es gibt keine ColorMap.

Tag = 277 (115.H)
Typ = KURZ
Die Anzahl der Komponenten pro Pixel. Diese Zahl ist 3 für RGB-Bilder, sofern keine zusätzlichen Muster vorhanden sind.

## Verweise ##

* [TIFF-Dateiformat – Wikipedia](https://en.wikipedia.org/wiki/TIFF)

