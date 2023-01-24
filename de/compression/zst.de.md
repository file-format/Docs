{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZST-Datei - komprimiertes Zstandard-Dateiformat",
  "description":"Erfahren Sie mehr über das ZST-Dateiformat und APIs, die ZST-Dateien erstellen und öffnen können.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Was ist eine ZST-Datei?

Eine ZST-Datei ist eine komprimierte Datei, die mit dem Komprimierungsalgorithmus Zstandard (zstd) generiert wird. Es ist eine komprimierte Datei, die vom Algorithmus mit verlustfreier Komprimierung erstellt wird. ZST-Dateien können verwendet werden, um verschiedene Dateitypen wie Datenbanken, Dateisysteme, Netzwerke und Spiele zu komprimieren. Der Z-Standard unterliegt [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), der den gesamten Komprimierungsmechanismus, den Medientyp und die Inhaltskodierung beschreibt.

## ZST-Dateiformat

ZST-Dateien werden im komprimierten Dateiformat auf Disc gespeichert. Der Komprimierungsmechanismus ist wie in RFC 8878 beschrieben, der RFC 8478 überholt.

## ZST-Rahmen

Eine ZST-Datei besteht aus einem oder mehreren Frames. Jeder Frame kann entweder ein Zstandard-Frame oder ein überspringbarer Frame sein. Ein Zstandard-Frame enthält komprimierte Daten, während ein überspringbarer Frame benutzerdefinierte Benutzermetadaten enthält.

### ZStandardrahmen

Ein Zstandard-Frame hat die folgende Struktur.

|Feld|Größe in Byte|
---|---|
|Magic_Number |4 Bytes|
|Frame_Header |2-14 Bytes|
|Daten_Block |n Bytes|
|[Weitere Datenblöcke] ||
|[Content_Checksum] |4 Bytes|

### Überspringbarer Rahmen

Ein überspringbarer Frame ermöglicht das Einfügen benutzerdefinierter Metadaten in einen Fluss verketteter Frames. Die Struktur eines überspringbaren Rahmens ist wie folgt.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 Bytes |4 Bytes |n Bytes|

## Verweise ##

* [RFC 8878 Zstandard-Komprimierung](https://www.rfc-editor.org/rfc/rfc8878)

