{
  "date" : "2022-01-23",
  "keywords" :[ "xz-Datei", "Dateiformat", "was ist eine xz-Datei", "Datei", "xz-Beispiel", "xz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ-Datei - XZ-komprimiertes Archiv",
  "description":"Erfahren Sie mehr über das XZ-Dateiformat und APIs, die XZ-Dateien erstellen und öffnen können.",
  "linktitle" :"XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Was ist eine XZ-Datei?

XZ ist ein komprimiertes Dateiformat, das den LZMA2-Komprimierungsalgorithmus verwendet. Es wurde als Ersatz für die gängigen Formate gzip und bzip2 entwickelt und bietet gegenüber diesen älteren Standards eine Reihe von Vorteilen. XZ-Dateien werden auf vielen Plattformen gut unterstützt und können schnell und einfach dekomprimiert werden. Obwohl sie nicht so verbreitet sind wie [ZIP](/de/compression/zip/)- oder [RAR](/de/compression/rar/)-Dateien, können XZ-Archive verwendet werden, um große Datenmengen zu speichern, ohne die Komprimierungsqualität zu beeinträchtigen. Wenn Sie große Dateien komprimieren oder dekomprimieren müssen, ist die XZ-Dateierweiterung eine Überlegung wert.

## XZ-Dateiformat

XZ-Dateien werden generiert und als Binärdateien auf der Disc gespeichert. Es verwendet den LZMA-Algorithmus zum Komprimieren von Daten und kann eine Komprimierungsrate von bis zu 50 % erreichen. XZ-Dateien werden normalerweise für Softwareverteilungen und Sicherungsarchive verwendet. Sie können mit dem XZ-Dienstprogramm dekomprimiert werden, das in den meisten Linux-Distributionen enthalten ist.

## Entpacken Sie XZ-Dateien unter Linux/Unix

Um XZ-Dateien zu entpacken, installieren Sie zuerst das Paket „xz-utils“:
```
$ sudo apt-get install xz-utils
```

Verwenden Sie den Befehl "unxz", um .xz-Dateien zu extrahieren:
```
$ unxz compressed_xz_file.xz
```

oder mit der Option --decompress von XZ verwenden:
```
$ xz --decompress compressed_xz_file.xz
```

## Verweise

* [XZ-Dienstprogramme](https://en.wikipedia.org/wiki/XZ_Utils)

