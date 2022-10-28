{
  "date" : "2019-10-11",
  "keywords" :[ "apng-Datei", "apng-Dateiformat", "was ist eine apng-Datei", "Datei", "apng-Beispiel", "apng-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG-Dateiformat - Animierte Grafikdatei für tragbare Netzwerke",
  "description":"Erfahren Sie mehr über das APNG-Dateiformat und APIs, die APNG-Dateien erstellen und öffnen können.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine APNG-Datei?

Eine Datei mit der Erweiterung .apng (Animated Portable Network Graphics) ist ein Rastergrafikformat und eine inoffizielle Erweiterung der Portable Network Graphics ([PNG](/de/image/png/) ). Es besteht aus mehreren Frames (jeweils ein PNG-Bild), die eine Animationssequenz darstellen. Dies ergibt eine ähnliche Visualisierung wie eine [GIF](/de/image/gif/)-Datei. APNG-Dateien unterstützen 24-Bit-Bilder und 8-Bit-Transparenz. APNG ist abwärtskompatibel mit nicht animierten GIF-Dateien. APNG-Dateien verwenden dieselbe .png-Erweiterung und können von Anwendungen wie Mozilla Firefox, Chrome mit APNG-Unterstützung, iMessage-Apps für iOS 10 geöffnet werden.

## Kurze Geschichte

* APNG-Spezifikationen wurden 2004 erstellt, um animierte PNG-Bilder zu unterstützen
* APNG-Decoder wurden mit viel kleinerer Größe und unter Verwendung der Rückseite des PNG-Decoders entwickelt
* Nach kontinuierlichen Überlegungen wurde ein neuer MIME-Typ image/apng formuliert, wobei die Erweiterung dieselbe wie .png statt .apng blieb
* APNG wurde von der PNG-Gruppe am 20. April 2007 aufgrund seiner Einheitlichkeit mit PNG-Bildern bei gleichzeitig unterschiedlichen Spezifikationen offiziell abgelehnt

## APNG-Dateiformat

APNG-Dateien werden als Binärdateien auf der Disc gespeichert und verwenden die erweiterten Spezifikationen von PNG für animierte Bilder. Das erste Bild einer APNG-Datei ist ein normaler PNG-Stream, der von PNG-Decodern zur Anzeige gelesen werden kann. Das APNG-Dateiformat folgt den PNG-Spezifikationen und Daten werden in Segmenten gespeichert, die Chunks genannt werden. APNG hat jedoch die folgenden neuen Chunks eingeführt:

„Animation Control Chunk (acTL)“ – Gibt an, dass es sich bei dieser Datei um eine animierte PNG-Datei und nicht um eine normale PNG-Datei handelt. Es fungiert als Markierung und kommt vor dem IDAT-Chunk. Es enthält auch die Anzahl der Frames und Informationen über die Zeiten, um die Animationen zu wiederholen

"Frame Control Chunk" - Tritt am Anfang jedes und Metadateninformationen wie Abmessungen, Position, Transparenzanwendung und Ersetzungsinformationen durch vorheriges oder nächstes Frame auf, sobald es vorbei ist.

„Frame Data Chunk“ – Speichert den Inhalt des Frames und beginnt mit einer Sequenznummer. Diese Sequenznummer hat dieselbe Struktur wie der IDAT-Chunk des Standardbilds.

{{< figure src="../APNG.png" alt="Animiertes PNG-APNG-Dateiformat" >}}

APNG ist abwärtskompatibel mit PNG, da die Spezifikationen der Seite so konzipiert wurden, dass eine Anwendung, die eine PNG-Datei liest, die Chunks, die sie nicht versteht, einfach ignorieren soll. Spezifikationen bezüglich Bittiefe, Farbtyp, Komprimierung, Filter, Interlace-Methoden und Paletteninformationen werden genauso verwendet wie die des standardmäßigen PNG-Formats.

## APNG vs. GIF

Da GIF bereits vorhanden ist und über einen langen Zeitraum verwendet wird, fragen Sie sich vielleicht, wie sich APNG von GIF unterscheidet. Im Folgenden finden Sie eine Reihe von Vergleichen zwischen APNG und GIF, die einen kurzen Überblick über beide Dateiformate geben.

||APNG|GIF|
---|---|---|
|Veröffentlicht|2004|1987|
|Farbtiefe|24 Bit|8 Bit|
|Bildrate|Unbegrenzt|10 Bilder pro Sekunde|
|Transparenz|Vollständig und teilweise|Vollständig|
|Komprimierung|Sehr gut|Gut|

## Verweise

* [APNG-Dateiformat](https://en.wikipedia.org/wiki/APNG)
* [Offizielle PNG-Formatspezifikationen](https://www.w3.org/TR/PNG/)

