{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - laajennettavissa oleva arkistotiedostomuoto",
  "description":"Opi XAR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XAR-tiedostoja.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Mikä on XAR-tiedosto?

Tiedosto, jonka laajennus on .xar (Extensible Archive Format), on UNIX-arkisto, joka voi olla pakatussa tai pakkaamattomassa muodossa. Sitä käytetään myös Mac OS -käyttöjärjestelmässä pakettien asentamiseen. XAR on avoimen lähdekoodin lähde, ja se on ollut osa Mac OS X 10.5 -käyttöjärjestelmää Safari-selaimen kanssa.

## XAR-tiedostomuoto

Tiedostossa [XAR](https://github.com/mackyle/xar/wiki/xarformat) on kolme pääaluetta.

 * Otsikko
 * Sisällysluettelo
 * Pino

### XAR-otsikko

XAR-otsikko on rakenteeltaan seuraava.

|Kenttä|Tietotyyppi|Koko tavuina|
---|---|---|
|Magic|Unsigned Int 32|4|
|Koko|Unsigned Int 16|2|
|Versio|Unsigned Int 16|2|
|TOC pituus pakattu|Unsigned Int 64|8|
|TOC:n pituus pakkaamaton|Unsigned Int 64|8|
|Tarkistussumma|Unsigned Int 32|4|
|Viestin tiivistelmän nimi |Null lopetettu||

XAR-otsikon C-rakenne voidaan määritellä seuraavasti.
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
Huomaa, että kaikki otsikon kentät (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) tallennetaan aina XAR-tiedostoihin verkkotavujärjestyksessä (eli big endian) järjestyksessä.

### XAR sisällysluettelo (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. Se on tallennettu tiedoston alkuun, joten se on helppo skannata arkiston läpi yksittäisen tiedoston purkamiseksi. XAR-arkiston avulla voit pakata/koodata arkiston yksittäisiä tiedostoja itsenäisesti käyttämällä erilaisia pakkausmenetelmiä, kuten [GZIP](/compression/gz/), [BZIP2](/compression/bz2/) ja muita vastaavia.  

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

### Kasa

Kasa alkaa heti pakatun tocin jälkeen. Se on jäsentämätön tietokasa, johon TOC viittaa. Sisältöluettelossa luetellut Offset-arvot alkavat keon alusta. Toc:n pituusarvot viittaavat kekoon tallennettujen tavujen todelliseen määrään (pakattu tai ei), kun taas koko-arvo viittaa kohteen poimimaan kokoon (tarvittaessa purkamisen jälkeen).

## Viitteet

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))


