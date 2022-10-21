{
  "date" : "2019-10-11",
  "keywords" :[ "bz2-Datei", "bz2-Dateiformat", "was ist eine bz2-Datei", "Datei", "bz2-Beispiel", "bz2-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Komprimiertes Dateiformat",
  "description":"Erfahren Sie, was eine BZ2-Datei und APIs sind, die BZ2-Dateien erstellen und öffnen können.",
  "linktitle" :"BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Was ist eine BZ2-Datei?

BZ2 sind komprimierte Dateien, die mit der Open-Source-Komprimierungsmethode [BZIP2](http://www.bzip.org/) generiert werden, hauptsächlich auf UNIX- oder Linux-Systemen. Es wird für die Komprimierung einer einzelnen Datei verwendet und ist nicht für die Archivierung mehrerer Dateien gedacht. Dies steht im Gegensatz zum TAR-Dateiformat auf denselben Plattformen, das mehrere Dateien in einer einzigen Datei archiviert, jedoch ohne Komprimierung. Als BZ2 komprimierte Dateien können mit Anwendungen wie [WinZip](https://www.winzip.com/win/en/) dekomprimiert werden. BZIP2 verwendet Run-Length Encoding (RLE) oder [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform)-Komprimierungsalgorithmus, um ein hohes Maß an Komprimierung zu erreichen.

## BZ2-Dateiformat

Für dieses Dateiformat sind keine formalen Spezifikationen verfügbar. Eine inoffizielle [Reverse Engineering-Spezifikation] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) zeigt jedoch, dass ein .bz2-Stream aus einem 4-Byte-Header besteht, dem gefolgt wird durch null oder mehr komprimierte Blöcke. Unmittelbar darauf folgt eine Stream-Ende-Markierung, die einen 32-Bit-CRC für den gesamten verarbeiteten Klartext-Stream enthält. Es gibt kein Padding zwischen den komprimierten Blöcken und alle Blöcke sind Bit-ausgerichtet.

## BZ2-Datei entpacken/extrahieren

Sie können eine BZ2-Datei unter Windows und Mac OS mit Software wie WinZip entpacken. Unter Linux der folgende Befehl im Terminal.

```
bzip2 -d filename.bz2
```

## Verweise

* [BZIP2-Formatspezifikationen](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

