{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Extensible Archive File Format",
  "description":"Další informace o formátu souboru XAR a rozhraních API, která mohou vytvářet a otevírat soubory XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Co je soubor XAR?

Soubor s příponou .xar (Extensible Archive Format) je archiv UNIX, který může být v komprimovaném nebo nekomprimovaném formátu. Používá se také na Mac OS pro instalaci balíčků. XAR je open-source a je součástí Mac OS X 10.5 pro použití s prohlížečem Safari.

## Formát souboru XAR

Soubor [XAR](https://github.com/mackyle/xar/wiki/xarformat) má tři hlavní oblasti.

* Záhlaví
* Obsah
* Hromada

### Hlavička XAR

Záhlaví XAR je strukturováno následovně.

|Pole|Typ dat|Velikost v bajtech|
---|---|---|
|Magic|Unsigned Int 32|4|
|Velikost|Nesigned Int 16|2|
|Verze|Unsigned Int 16|2|
|TOC délka komprimovaná|bez znaménka int 64|8|
|TOC Délka Nekomprimovaný|Nepodepsaný Int 64|8|
|Kontrolní součet|Nepodepsané mezinár. 32|4|
|Název přehledu zpráv |Null ukončeno||

C struktura hlavičky XAR může být definována následovně.
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
Všimněte si, že všechna pole hlavičky (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) jsou vždy uložena v souborech XAR v pořadí síťových bajtů (aka big endian).

### Obsah XAR (TOC)

Obsah je dokument XML, který je (a musí) být kódován jako UTF-8. Je uložen na začátku souboru, což usnadňuje procházení archivu a extrahování jednotlivých souborů. Archiv XAR vám umožňuje komprimovat/kódovat jednotlivé soubory v archivu nezávisle pomocí různých kompresních schémat, jako je [GZIP](/cs/compression/gz/), [BZIP2](/cs/compression/bz2/) a další podobná.

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

### Hromada

Hromada začíná ihned po komprimovaném toc. Je to nestrukturovaná hromada dat, na kterou odkazuje TOC. Hodnoty Offset uvedené v TOC začínají od začátku haldy. Hodnoty délky v toc odkazují na skutečný počet bajtů uložených v haldě (komprimované nebo nekomprimované), zatímco hodnota velikosti odkazuje na extrahovanou velikost položky (po případné dekomprimaci).

## Reference

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR – Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

