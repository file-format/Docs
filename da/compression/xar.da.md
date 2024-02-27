{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - Extensible Archive File Format",
  "description":"Lær om XAR-filformat og API'er, der kan oprette og åbne XAR-filer.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-da",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Hvad er en XAR fil?

En fil med filtypenavnet .xar (Extensible Archive Format) er et UNIX-arkiv, der kan være i komprimeret eller ikke-komprimeret format. Det bruges også på Mac OS til installation af pakker. XAR er open source og har været en del af Mac OS X 10.5 til brug med Safari-browseren.

## XAR filformat

En [XAR](https://github.com/mackyle/xar/wiki/xarformat)-fil har tre hovedområder.

 * Header
 * Indholdsfortegnelse
 * Dynge

### XAR Header

XAR-headeren er struktureret som følger.

|Felt|Datatype|Størrelse i bytes|
---|---|---|
|Magic|Usigned Int 32|4|
|Størrelse|Usigned Int 16|2|
|Version|Usigned Int 16|2|
|TOC Længde Komprimeret|Usigned Int 64|8|
|TOC Længde Ukomprimeret|Usigneret Int 64|8|
|Checksum|Usigned Int 32|4|
|Beskedsammendragsnavn |Nul afsluttet||

C-strukturen af XAR-headeren kan defineres som følger.
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
Bemærk, at alle felter i overskriften (magi, størrelse, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) altid er gemt i XAR-filer i netværksbyte (aka big endian) rækkefølge.

### XAR Indholdsfortegnelse (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. Det er gemt i begyndelsen af filen, hvilket gør det nemt at scanne gennem arkivet for at udpakke individuelle filer. XAR-arkivet lader dig komprimere/kode de individuelle filer i arkivet uafhængigt ved hjælp af forskellige komprimeringsskemaer såsom [GZIP](/compression/gz/), [BZIP2](/compression/bz2/) og andre lignende.  

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

### Dynge

Heapen starter umiddelbart efter den komprimerede toc. Det er en ustruktureret bunke data, der refereres til af TOC. Offset-værdierne, der er angivet i TOC, starter fra begyndelsen af heapen. Længdeværdierne i toc'en refererer til det faktiske antal bytes, der er gemt i heapen (komprimeret eller ej), hvorimod størrelsesværdien refererer til den ekstraherede størrelse af emnet (efter dekomprimering, hvis det er nødvendigt).

## Referencer

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))


