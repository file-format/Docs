{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - rozszerzalny format pliku archiwum",
  "description":"Poznaj format pliku XAR i interfejsy API, które mogą tworzyć i otwierać pliki XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Czym jest plik XAR?

Plik z rozszerzeniem .xar (Extensible Archive Format) to archiwum systemu UNIX, które może być w formacie skompresowanym lub nieskompresowanym. Jest również używany w systemie Mac OS do instalacji pakietów. XAR jest open source i był częścią systemu Mac OS X 10.5 do użytku z przeglądarką Safari.

## Format pliku XAR

Plik [XAR](https://github.com/mackyle/xar/wiki/xarformat) ma trzy główne regiony.

* Nagłówek
* Spis treści
* Sterta

### Nagłówek XAR

Nagłówek XAR ma następującą strukturę.

|Pole|Typ danych|Rozmiar w bajtach|
---|---|---|
|Magia|Bez znaku Int 32|4|
|Rozmiar|Bez znaku Int 16|2|
|Wersja|Bez znaku Int 16|2|
|Długość spisu treści skompresowana|Bez znaku Int 64|8|
|Długość TOC Nieskompresowany|Bez znaku Int 64|8|
|Suma kontrolna|Bez znaku Int 32|4|
|Nazwa skrótu wiadomości |Null Zakończona||

Strukturę C nagłówka XAR można zdefiniować w następujący sposób.
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
Zauważ, że wszystkie pola nagłówka (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) są zawsze przechowywane w plikach XAR w kolejności bajtów sieciowych (inaczej big endian).

### XAR Spis treści (TOC)

Spis treści to dokument XML, który jest (i musi) być zakodowany w UTF-8. Jest przechowywany na początku pliku, co ułatwia przeglądanie archiwum w celu wyodrębnienia pojedynczego pliku. Archiwum XAR umożliwia niezależne kompresowanie/kodowanie poszczególnych plików w archiwum przy użyciu różnych schematów kompresji, takich jak [GZIP](/pl/compression/gz/), [BZIP2](/pl/compression/bz2) i inne podobne.

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

### Sterta

Sterta rozpoczyna się natychmiast po skompresowanym toc. Jest to nieustrukturyzowana sterta danych, do których odwołuje się spis treści. Wartości przesunięcia wymienione w spisie treści zaczynają się od początku sterty. Wartości długości w toc odnoszą się do rzeczywistej liczby bajtów przechowywanych na stercie (skompresowane lub nie), podczas gdy wartość rozmiaru odnosi się do wyodrębnionego rozmiaru elementu (po dekompresji, jeśli to konieczne).

## Bibliografia

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

