{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Erweiterbares Archivdateiformat",
  "description":"Erfahren Sie mehr über das XAR-Dateiformat und APIs, die XAR-Dateien erstellen und öffnen können.",
  "linktitle" :"XAR",
  "menu" : {
    "docs" : {
"identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Was ist eine XAR-Datei?

Eine Datei mit der Erweiterung .xar (Extensible Archive Format) ist ein UNIX-Archiv, das in komprimiertem oder nicht komprimiertem Format vorliegen kann. Es wird auch unter Mac OS zur Installation von Paketen verwendet. XAR ist Open Source und Teil von Mac OS X 10.5 für die Verwendung mit dem Safari-Browser.

## XAR-Dateiformat

Eine [XAR](https://github.com/mackyle/xar/wiki/xarformat)-Datei hat drei Hauptbereiche.

* Header
* Inhaltsverzeichnis
* Haufen

### XAR-Header

Der XAR-Header ist wie folgt aufgebaut.

|Feld|Datentyp|Größe in Bytes|
---|---|---|
|Magic|Unsigned Int 32|4|
|Größe|Unsigned Int 16|2|
|Version|Unsigned Int 16|2|
|TOC-Länge komprimiert|Unsigned Int 64|8|
|TOC-Länge unkomprimiert|Unsigned Int 64|8|
|Prüfsumme|Unsigned Int 32|4|
|Message Digest Name |Null beendet||

Die C-Struktur des XAR-Headers kann wie folgt definiert werden.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Beachten Sie, dass alle Felder des Headers (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) immer in XAR-Dateien in Netzwerk-Byte-Reihenfolge (auch bekannt als Big Endian) gespeichert werden.

### XAR-Inhaltsverzeichnis (TOC)

Das Inhaltsverzeichnis ist ein XML-Dokument, das als UTF-8 codiert ist (und muss). Es wird am Anfang der Datei gespeichert, was es einfach macht, das Archiv zu durchsuchen, um einzelne Dateien zu extrahieren. Mit dem XAR-Archiv können Sie die einzelnen Dateien im Archiv unabhängig voneinander komprimieren/codieren, indem Sie verschiedene Komprimierungsschemata wie [GZIP](/de/compression/gz/), [BZIP2](/de/compression/bz2) und andere ähnliche verwenden.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### Haufen

Der Heap beginnt unmittelbar nach dem komprimierten toc. Es ist ein unstrukturierter Datenhaufen, auf den das Inhaltsverzeichnis verweist. Die im Inhaltsverzeichnis aufgelisteten Offset-Werte beginnen am Anfang des Heaps. Die Längenwerte im toc beziehen sich auf die tatsächliche Anzahl der im Heap gespeicherten Bytes (komprimiert oder nicht), während sich der Größenwert auf die extrahierte Größe des Elements bezieht (falls erforderlich nach Dekomprimierung).

## Verweise

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

