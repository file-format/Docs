{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR — paplašināms arhīva faila formāts",
  "description":"Uzziniet par XAR faila formātu un API, kas var izveidot un atvērt XAR failus.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Kas ir XAR fails?

Fails ar paplašinājumu .xar (Extensible Archive Format) ir UNIX arhīvs, kas var būt saspiestā vai nesaspiestā formātā. To izmanto arī Mac OS pakotņu instalēšanai. XAR ir atvērtā koda un ir daļa no Mac OS X 10.5 lietošanai ar Safari pārlūkprogrammu.

## XAR faila formāts

Failam [XAR](https://github.com/mackyle/xar/wiki/xarformat) ir trīs galvenie reģioni.

 * Virsraksts
 * Satura rādītājs
 * Kaudze

### XAR galvene

XAR galvene ir strukturēta šādi.

|Lauks|Datu tips|Izmērs baitos|
---|---|---|
|Magic|Unsigned Int 32|4|
|Izmērs|Unsigned Int 16|2|
|Versija|Unsigned Int 16|2|
|TOC garums saspiests|Unsigned Int 64|8|
|TOC garums nesaspiests|Unsigned Int 64|8|
|Kontrolsumma|Unsigned Int 32|4|
|Ziņojuma apkopojuma nosaukums |Null pārtraukts||

XAR galvenes C struktūru var definēt šādi.
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
Ņemiet vērā, ka visi galvenes lauki (maģija, izmērs, versija, toc_length_compressed, toc_length_uncompressed, cksum_alg) vienmēr tiek saglabāti XAR failos tīkla baitu (aka big endian) secībā.

### XAR satura rādītājs (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. Tas tiek saglabāts faila sākumā, padarot to viegli skenēšanu arhīvā, lai izvilktu atsevišķu failu. XAR arhīvs ļauj saspiest/kodēt atsevišķus arhīva failus neatkarīgi, izmantojot dažādas saspiešanas shēmas, piemēram, [GZIP](/compression/gz/), [BZIP2](/compression/bz2/) un citas līdzīgas.  

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

### Kaudze

Kaudze sākas uzreiz pēc saspiestā toc. Tā ir nestrukturēta datu kaudze, uz kuru atsaucas TOC. TOC norādītās nobīdes vērtības sākas no kaudzes sākuma. Toc garuma vērtības attiecas uz faktisko kaudzē saglabāto baitu skaitu (saspiests vai nesaspiests), savukārt lieluma vērtība attiecas uz izvilkto vienuma izmēru (pēc atspiešanas, ja nepieciešams).

## Atsauces

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR — Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))


