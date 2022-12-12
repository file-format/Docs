{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Format de fișier arhivă extensibil",
  "description":"Aflați despre formatul de fișier XAR și despre API-urile care pot crea și deschide fișiere XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Ce este un fișier XAR?

Un fișier cu extensia .xar (Extensible Archive Format) este o arhivă UNIX care poate fi în format comprimat sau necomprimat. De asemenea, este folosit pe Mac OS pentru instalarea pachetelor. XAR este open source și a făcut parte din Mac OS X 10.5 pentru utilizare cu browser-ul Safari.

## Format de fișier XAR

Un fișier [XAR](https://github.com/mackyle/xar/wiki/xarformat) are trei regiuni principale.

* Antet
* Cuprins
* grămada

### Antet XAR

Antetul XAR este structurat după cum urmează.

|Câmp|Tip de date|Dimensiune în octeți|
---|---|---|
|Magie|Unsigned Int 32|4|
|Dimensiune|Unsigned Int 16|2|
|Versiune|Unsigned Int 16|2|
|TOC Length Compressed|Unsigned Int 64|8|
|TOC Length UnCompressed|Unsigned Int 64|8|
|Checksum|Unsigned Int 32|4|
|Nume rezumat mesaj |Null terminat||

Structura C a antetului XAR poate fi definită după cum urmează.
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
Rețineți că toate câmpurile antetului (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) sunt întotdeauna stocate în fișiere XAR în ordinea octeților de rețea (alias big endian).

### XAR Cuprins (TOC)

Cuprinsul este un document XML care este (și trebuie) codificat ca UTF-8. Este stocat la începutul fișierului, facilitând scanarea arhivei pentru a extrage fișierul individual. Arhiva XAR vă permite să comprimați/codați fișierele individuale din arhivă în mod independent, folosind diferite scheme de compresie, cum ar fi [GZIP](/ro/compression/gz/), [BZIP2](/ro/compression/bz2) și altele similare.

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

### Heap

Heapul începe imediat după toc comprimat. Este o grămadă nestructurată de date la care face referire TOC. Valorile Offset enumerate în TOC încep de la începutul heap-ului. Valorile lungimii din toc se referă la numărul real de octeți stocați în heap (comprimați sau nu), în timp ce valoarea mărimii se referă la dimensiunea extrasă a elementului (după decomprimare, dacă este necesar).

## Referințe

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

