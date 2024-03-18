{
  "date" : "2021-04-08",
  "keywords" :[ "lzma file", "lzma file format", "was ist eine lzma file", "file", "lzma example", "lzma file extension", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA-komprimiertes Dateiformat",
  "description":"Was ist eine LZMA-Datei und APIs, die LZMA-Dateien erstellen und öffnen können.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Was ist eine LZMA-Datei?

Eine Datei mit der Erweiterung .lzma ist eine komprimierte Archivdatei, die mit der Komprimierungsmethode LZMA (Lempel-Ziv-Markov-Kettenalgorithmus) erstellt wurde. Diese werden hauptsächlich auf Unix-Betriebssystemen gefunden/verwendet und ähneln anderen Komprimierungsalgorithmen wie [ZIP](/de/compression/zip/) zum Minimieren der Dateigröße. LZMA ist ein älteres Dateiformat, das durch das .xz-Format ersetzt wird oder wurde. Der MIME-Typ des .lzma-Formats ist \`application/x-lzma'. Dieses Dateiformat wurde von Igor Pavlov für die Verwendung im LZMA SDK entwickelt.

## LZMA-Dateiformat

Die LZMA-Datei besteht aus zwei Hauptteilen:

1. Kopfzeile
1. Komprimierte Daten


### LZMA-Header

Die LZMA-Dateien haben einen 13-Byte-Header, dem die komprimierten LZMA-Daten folgen. Der LZMA-Header besteht aus:

* Eigenschaften
* Wörterbuchgröße
* Unkomprimierte Größe

#### LZMA-Header-Eigenschaften

Das Feld Eigenschaften enthält drei Eigenschaften. In Klammern steht eine Abkürzung, gefolgt vom Wertebereich der Eigenschaft. Das Feld besteht aus

1) die Anzahl der wörtlichen Kontextbits (lc, [0, 8]);
2) die Anzahl der Literalpositionsbits (lp, [0, 4]); und
3) die Anzahl der Positionsbits (pb, [0, 4]).

#### Größe des LZMA-Wörterbuchs

Dies wird als vorzeichenlose 32-Bit-Little-Endian-Ganzzahl mit Werten zwischen 2^n und 2^n + 2^(n-1) gespeichert. LZMA Utils kann Dateien mit jeder Wörterbuchgröße dekomprimieren.

#### Unkomprimierte Größe
Die unkomprimierte Größe wird als vorzeichenlose 64-Bit-Little-Endian-Ganzzahl gespeichert. Ein spezieller Wert von 0xFFFF_FFFF_FFFF_FFFF gibt an, dass die unkomprimierte Größe unbekannt ist. Der Wert wird durch die End-of-Payload-Markierung (\*) dargestellt, wenn und nur wenn die unkomprimierte Größe unbekannt ist.

## Verweise

* [Lempel-Ziv-Markov-Kettenalgorithmus](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
