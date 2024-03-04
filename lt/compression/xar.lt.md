{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR – išplečiamo archyvo failo formatas",
  "description":"Sužinokite apie XAR failo formatą ir API, kurios gali kurti ir atidaryti XAR failus.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Kas yra XAR failas?

Failas su plėtiniu .xar (Extensible Archive Format) yra UNIX archyvas, kuris gali būti suspausto arba nesuspausto formato. Jis taip pat naudojamas Mac OS paketams įdiegti. XAR yra atvirojo kodo ir buvo Mac OS X 10.5 dalis, skirta naudoti su Safari naršykle.

## XAR failo formatas

Failas [XAR](https://github.com/mackyle/xar/wiki/xarformat) turi tris pagrindinius regionus.

 * Antraštė
 * Turinys
 * Krūva

### XAR antraštė

XAR antraštės struktūra yra tokia.

|Laukas|Duomenų tipas|Dydis baitais|
---|---|---|
|Magic|Unsigned Int 32|4|
|Dydis|Unsigned Int 16|2|
|Versija|Unsigned Int 16|2|
|TOC ilgis suspaustas|Unsigned Int 64|8|
|TOC ilgis nesuspaustas|Unsigned Int 64|8|
|Kontrolinė suma|Unsigned Int 32|4|
|Pranešimo santraukos pavadinimas |Nulis nutrauktas||

XAR antraštės C struktūrą galima apibrėžti taip.
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
Atminkite, kad visi antraštės laukai (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) visada saugomi XAR failuose tinklo baitų (dar žinomas kaip big endian) tvarka.

### XAR turinys (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. Jis saugomas failo pradžioje, todėl jį lengva nuskaityti per archyvą, kad būtų galima išskirti atskirą failą. XAR archyvas leidžia atskirai suspausti / užkoduoti atskirus archyvo failus, naudojant skirtingas glaudinimo schemas, pvz., [GZIP](/compression/gz/), [BZIP2](/compression/bz2/) ir kitas panašias.  

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

### Krūva

Krūva prasideda iškart po suspausto toc. Tai nestruktūrizuota duomenų krūva, kurią nurodo TOC. TOC nurodytos poslinkio reikšmės prasideda nuo krūvos pradžios. Toc ilgio reikšmės nurodo tikrąjį krūvoje saugomų baitų skaičių (suglaudintą ar ne), o dydžio reikšmė nurodo išskirtą elemento dydį (jei reikia, išglaudinus).

## Nuorodos

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR – Vikipedija](https://en.wikipedia.org/wiki/Xar_(archiver))


