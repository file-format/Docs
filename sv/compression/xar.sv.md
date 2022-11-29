{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Extensible Archive File Format",
  "description":"Läs mer om XAR-filformat och API:er som kan skapa och öppna XAR-filer.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Vad är en XAR fil?

En fil med tillägget .xar (Extensible Archive Format) är ett UNIX-arkiv som kan vara i komprimerat eller icke-komprimerat format. Det används även på Mac OS för installation av paket. XAR är öppen källkod och har varit en del av Mac OS X 10.5 för användning med webbläsaren Safari.

## XAR filformat

En [XAR](https://github.com/mackyle/xar/wiki/xarformat) fil har tre huvudregioner.

* Header
* Innehållsförteckning
* Högen

### XAR Header

XAR-huvudet är strukturerat enligt följande.

|Fält|Datatyp|Storlek i byte|
---|---|---|
|Magic|Osignerad Int 32|4|
|Storlek|Osignerad Int 16|2|
|Version|Osignerad Int 16|2|
|TOC Längd Komprimerad|Osignerad Int 64|8|
|TOC Längd Okomprimerad|Osignerad Int 64|8|
|Checksum|Osignerad Int 32|4|
|Meddelandesammandragsnamn |Null avslutad||

C-strukturen för XAR-huvudet kan definieras enligt följande.
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
Observera att alla fält i rubriken (magi, storlek, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) alltid lagras i XAR-filer i nätverksbyte-ordning (aka big endian).

### XAR Innehållsförteckning (TOC)

Innehållsförteckningen är ett XML-dokument som är (och måste) kodas som UTF-8. Den lagras i början av filen, vilket gör det enkelt att skanna igenom arkivet för att extrahera enskild fil. XAR-arkivet låter dig komprimera/koda de enskilda filerna i arkivet oberoende med hjälp av olika komprimeringsscheman såsom [GZIP](/sv/compression/gz/), [BZIP2](/sv/compression/bz2) och andra liknande.

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

### Högen

Högen startar omedelbart efter den komprimerade toc. Det är en ostrukturerad hög med data som refereras av TOC. Offsetvärdena som anges i TOC börjar från början av högen. Längdvärdena i toc hänvisar till det faktiska antalet byte lagrade i heapen (komprimerade eller inte) medan storleksvärdet hänvisar till den extraherade storleken på objektet (efter dekomprimering vid behov).

## Referenser

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

