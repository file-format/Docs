{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - Formáid Chomhaid Cartlainne Inmhínithe",
  "description":"Foghlaim faoi fhormáid comhaid XAR agus APIanna ar féidir leo comhaid XAR a chruthú agus a oscailt.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-ga",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Cad is comhad XAR ann?

Is cartlann UNIX é comhad a bhfuil an iarmhír .xar (Formáid Chartlainne Leathnaithe air) ann a d’fhéadfadh a bheith i bhformáid chomhbhrúite nó neamh-chomhbhrúite. Úsáidtear é freisin ar Mac OS chun pacáistí a shuiteáil. Is foinse oscailte é XAR agus bhí sé mar chuid de Mac OS X 10.5 le húsáid le brabhsálaí Safari.

## Formáid Chomhaid XAR

Tá trí phríomhréigiún i gcomhad [XAR](https://github.com/mackyle/xar/wiki/xarformat).

 * Ceanntásc
 * Clár ábhair
 * Carn

### Ceanntásc XAR

Tá an ceanntásc XAR struchtúrtha mar seo a leanas.

|Réimse|Cineál Sonraí|Méid i mBeart|
---|---|---|
|Draíocht|Int gan síniú 32|4|
|Méid|Int gan síniú 16|2|
|Leagan|Int gan síniú 16|2|
|Fad TOC Comhbhrúite|Int gan síniú 64|8|
|Fad TOC Neamh-chomhbhrúite|Int gan síniú 64|8|
|Seiceáil|Int gan síniú 32|4|
|Ainm Achoimre na Teachtaireachta |Críochnaithe ar neamhní||

Is féidir struchtúr C ceanntásc XAR a shainiú mar seo a leanas.
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
Tabhair faoi deara go stóráiltear gach réimse den cheanntásc (draíochta, méid, leagan, toc_length_compressed, toc_length_uncompressed, cksum_alg) i gcomhaid XAR in ord beart líonra (aka big endian).

### Clár Ábhar XAR (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. Stóráiltear é i dtús an chomhaid, rud a fhágann go bhfuil sé éasca é a scanadh tríd an gcartlann chun comhad aonair a bhaint as. Ligeann cartlann XAR duit na comhaid aonair sa chartlann a chomhbhrú/ionchódú go neamhspleách agus úsáid á baint as scéimeanna comhbhrú difriúla ar nós [GZIP](/compression/gz/), [BZIP2](/compression/bz2/), agus eile dá samhail.  

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

### Charn

Tosaíonn an carn díreach tar éis an toc comhbhrúite. Is carn neamhstruchtúrtha sonraí é a ndéanann an TOC tagairt dó. Tosaíonn na luachanna Fritháireamh atá liostaithe in TOC ó thús an charn. Tagraíonn na luachanna faid sa toc don líon iarbhír beart atá stóráilte sa charn (comhbhrúite nó nach bhfuil) ach tagraíonn an luach méide do mhéid eastósctha na míre (tar éis dí-chomhbhrúite más gá).

## Tagairtí

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR - Vicipéid](https://en.wikipedia.org/wiki/Xar_(archiver))


