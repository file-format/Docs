{
  "date" : "2021-04-08",
  "keywords" :[ "lz4-Datei", "lz4-Dateiformat", "was ist eine lz4-Datei", "Datei", "lz4-Beispiel", "lz4-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 komprimiertes Dateiformat",
  "description":"Erfahren Sie mehr über das LBR-Dateiformat und APIs, die LZ4-Dateien erstellen und öffnen können.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Was ist eine LZ4-Datei?

Eine Datei mit der Erweiterung .lz4 ist eine komprimierte Archivdatei, die mit Anwendungen/Dienstprogrammen erstellt wurde, die die [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))-Komprimierung unterstützen. Der LZ4-Algorithmus konzentriert sich auf den Kompromiss zwischen Geschwindigkeit und Komprimierungsverhältnis. Komprimierte LZ4-Archive können mit dem LZ4-Befehlszeilendienstprogramm erstellt und mit demselben dekomprimiert werden.

## LZ4-Dateiformat

Das auf dem LZ4-Komprimierungsalgorithmus basierende LZ4-Dateiformat ist unabhängig von CPU-Typ, Betriebssystem, Dateisystem und Zeichensatz. Es eignet sich für die Dateikomprimierung und Streaming-Komprimierung mit dem LZ4-Algorithmus. Die anfängliche Implementierung des LZ4-Formats wurde 2011 von Yann Collet in der Sprache [C](/de/programming/c/) durchgeführt und ist als Referenz für Entwickler auf [Github](https://github.com/lz4/lz4) verfügbar. .

### LZ4-Rahmenformat

Die allgemeine Struktur des LZ4-Dateiformats ist wie unten gezeigt.

|MagicNb|F. Deskriptor| Block|(...)|EndMark |C. Prüfsumme|
---|---|---|---|---|---|
|4 Bytes| 3-15 Byte||| 4 Bytes| 0-4 Bytes|

#### Magische Zahl

4 Bytes, Little-Endian-Format. Wert: 0x184D2204

#### Frame-Deskriptor

Der Frame Descriptor besteht aus 3 bis 15 Bytes und ist der wichtigste Teil der Spezifikationen. Zusammen werden die Felder Magic_Number und Frame_Descriptor als LZ4-Frame-Header bezeichnet, und ihre Größe variiert zwischen 7 und 19 Bytes. Es ist wie unten gezeigt.

|FLG| BD| (Inhaltsgröße)| (Wörterbuch-ID)| HC|
---|---|---|---|---|
|1 Byte| 1 byte| 0 - 8 Bytes| 0 - 4 Bytes| 1 byte|

#### Datenblöcke

Jeder Datenblock folgt der folgenden Reihenfolge.

|Blockgröße| Daten| (Prüfsumme blockieren)|
---|---|---|
|4 Bytes| |0 - 4 Bytes|

#### EndMark

Der Fluss der Blöcke endet, wenn auf den letzten Datenblock der 32-Bit-Wert 0x00000000 folgt.

#### Inhaltsprüfsumme

Die Content_Checksum verifiziert die Gültigkeit des korrekt decodierten Inhalts und wird unter Verwendung des Ergebnisses des xxHash-32-Algorithmus ausgeführt. Es validiert die Ergebnisse der erfolgreichen Übertragung aller Blöcke in der richtigen Reihenfolge und ohne Fehler.

## Verweise

* [LZ4-Rahmenformat](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4-Komprimierungsalgorithmus – Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

