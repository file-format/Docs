{
  "date" : "2021-04-08",
  "keywords" :[ "lz-Datei", "lz-Dateiformat", "was ist eine lz-Datei", "Datei", "lz-Beispiel", "lz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - komprimiertes Lzip-Dateiformat",
  "description":"Erfahren Sie mehr über das LZ-Dateiformat und APIs, die LZ-Dateien erstellen und öffnen können.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Was ist eine LZ-Datei?

Eine Datei mit der Erweiterung .lz ist eine komprimierte Archivdatei, die mit Lzip erstellt wurde, einem kostenlosen Befehlszeilentool für die Komprimierung. Es unterstützt die Verkettung, um Support-Dateien zu komprimieren. LZ-Dateien haben den Medientyp application/lzip und unterstützen höhere Komprimierungsraten als [BZ2](/de/compression/bz2/). LZ basieren auf dem LZMA-Algorithmus (Lempel-Ziv-Markov-Kette) und enthalten eine 32-Bit-CRC-Prüfsumme und Ident-Bytes zur Überprüfung der Integrität der Datei.

## LZMA-komprimiertes Format

Das komprimierte LZMA-Format besteht aus einem komprimierten Bitstrom, der mit einem adaptiven Binärbereichscodierer codiert wird. Der Stream wird in Pakete aufgeteilt. Jedes Paket beschreibt entweder ein einzelnes Byte oder eine LZ77-Folge. Die Länge und Entfernung jedes Pakets wird implizit oder explizit codiert.

Die sieben Arten von Paketen sind wie folgt ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Gepackter Code (Bitfolge) |Paketname |Paketbeschreibung|
---|---|---|
|0 + byteCode| LIT| Ein einzelnes Byte, das mit einem adaptiven binären Bereichscodierer codiert wurde.|
|1+0 + Länge + Abstand| ÜBEREINSTIMMUNG| Eine typische LZ77-Sequenz, die Sequenzlänge und -abstand beschreibt.|
|1+1+0+0| KURZREPARATUR| Eine Ein-Byte-LZ77-Sequenz. Die Entfernung entspricht der zuletzt verwendeten LZ77-Entfernung.|
|1+1+0+1 + Länge| LONGREP[0]| Eine LZ77-Sequenz. Die Entfernung entspricht der zuletzt verwendeten LZ77-Entfernung.|
|1+1+1+0 + Länge| LONGREP[1]| Eine LZ77-Sequenz. Die Entfernung entspricht der vorletzten verwendeten LZ77-Entfernung.|
|1+1+1+1+0 + Länge| LONGREP[2]| Eine LZ77-Sequenz. Die Entfernung entspricht der drittletzten verwendeten LZ77-Entfernung.|
|1+1+1+1+1 + Länge| LONGREP[3]| Eine LZ77-Sequenz. Die Entfernung entspricht der viertletzten verwendeten LZ77-Entfernung.|


## Verweise

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://de.wikipedia.org/wiki/Lzip)

