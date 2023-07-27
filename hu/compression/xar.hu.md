{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - bővíthető archív fájlformátum",
  "description":"További információ az XAR fájlformátumról és az API-król, amelyek XAR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Mi az a XAR fájl?

A .xar (Extensible Archive Format) kiterjesztésű fájl UNIX archívum, amely lehet tömörített vagy nem tömörített formátumú. Mac OS rendszeren is használják csomagok telepítésére. Az XAR nyílt forráskódú, és a Mac OS X 10.5 része a Safari böngészővel való használatra.

## XAR fájlformátum

A [XAR](https://github.com/mackyle/xar/wiki/xarformat) fájlnak három fő régiója van.

* Fejléc
* Tartalomjegyzék
* Halom

### XAR fejléc

Az XAR fejléc a következőképpen épül fel.

|Mező|Adattípus|Méret bájtban|
---|---|---|
|Magic|Unsigned Int 32|4|
|Méret|Unsigned Int 16|2|
|Verzió|Unsigned Int 16|2|
|TOC hossza tömörítve|Unsigned Int 64|8|
|TOC hossza tömörítetlen|Unsigned Int 64|8|
|Ellenőrző összeg|Unsigned Int 32|4|
|Üzenetkivonat neve |Null megszűnt||

Az XAR fejléc C szerkezete a következőképpen definiálható.
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
Vegye figyelembe, hogy a fejléc összes mezője (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) mindig XAR-fájlokban tárolódik hálózati bájt (más néven big endian) sorrendben.

### XAR tartalomjegyzék (TOC)

A tartalomjegyzék egy XML dokumentum, amely UTF-8 kódolású (és kell). A fájl elején tárolódik, így könnyen átvizsgálható az archívumban az egyes fájlok kibontásához. Az XAR archívum lehetővé teszi az archívumban lévő egyes fájlok önálló tömörítését/kódolását különböző tömörítési sémák, például [GZIP](/hu/compression/gz/), [BZIP2](/hu/compression/bz2/) és más hasonlók használatával.

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

### Halom

A kupac közvetlenül a tömörített toc után kezdődik. Ez egy strukturálatlan adathalom, amelyre a TOC hivatkozik. A TOC-ban felsorolt Offset értékek a kupac elejétől kezdődnek. A toc-ban lévő hosszértékek a kupacban tárolt bájtok tényleges számára vonatkoznak (tömörítve vagy nem), míg a méretérték az elem kibontott méretére vonatkozik (szükség esetén kicsomagolás után).

## Hivatkozások

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR – Wikipédia](https://en.wikipedia.org/wiki/Xar_(archiver))

