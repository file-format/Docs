{
  "date" : "2019-10-11",
  "keywords" :[ "tbz-Datei", "tbz-Dateiformat", "was ist eine tbz-Datei", "Datei", "tbz-Beispiel", "tbz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip-komprimiertes Tar-Archiv",
  "description":"Erfahren Sie mehr über das TBZ-Dateiformat und APIs, die TBZ-Dateien erstellen und öffnen können.",
  "linktitle" :"TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Was ist eine TBZ-Datei?

Eine Datei mit der Erweiterung .tbz ist ein komprimiertes Archiv, das die BZIP-Komprimierung verwendet, um die Größe der Inhaltsdateien zu reduzieren. Die TBZ-Dateien sind eigentlich UNIX [TAR](/de/compression/tar/) archivierte Dateien, die dann mit BZIP komprimiert werden. Die neueste Komprimierung der zweiten Ebene ist [BZIP2](/de/compression/bz2/), die BZIP ersetzt hat. Das TBZ-Dateiformat eignet sich zum Übertragen großer Dateien. TBZ-Dateien können mit Softwareanwendungen wie 7-Zip, PeaZip und jZip geöffnet/extrahiert werden. Linux- und macOS-Benutzer können eine TBZ auch mit dem BZIP2-Befehl aus einem Terminalfenster öffnen.

## TBZ-Dateiformat

TBZ-Dateien sind eigentlich komprimierte Archive, die mit BZIP/[BZIP2](/de/compression/bz2)-Komprimierung erstellt wurden. Für dieses Dateiformat sind keine formalen Spezifikationen verfügbar. Eine inoffizielle [Reverse Engineering-Spezifikation] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) zeigt jedoch, dass ein .bz2-Stream aus einem 4-Byte-Header besteht, dem gefolgt wird durch null oder mehr komprimierte Blöcke.

## Verweise ##

* [BZIP2-Formatspezifikationen](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

