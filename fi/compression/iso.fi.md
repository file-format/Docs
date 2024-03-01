{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - levykuvatiedostomuoto",
  "description":"Mikä on ISO-tiedosto ja API:t, jotka voivat luoda ja avata ISO-tiedostoja.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Mikä on ISO-tiedosto?

Tiedosto, jonka tunniste on .iso, on pakkaamaton arkistolevykuvatiedosto, joka edustaa optisen levyn, kuten CD- tai DVD-levyn, koko tiedon sisältöä. Standardiin [ISO-9660](https://www.iso.org/standard/17505.html) perustuva ISO-kuvatiedostomuoto sisältää levyn tiedot ja siihen tallennetut tiedostojärjestelmätiedot. ISO-tiedostojen kyky sisältää tarkan jäljennöksen sisällöstä tekee niistä täydellisen tiedostotyypin CD-/DVD-kopioiden luomiseen, ja niitä käytetään useimmiten käynnistystietojen tallentamiseen asennusta varten. Useimmiten ISO-tiedostot poltetaan USB-/CD-/DVD-levylle käynnistettäväksi sisällöksi koneen käynnistämistä varten asennusta varten. ISO-tiedostoissa on MIME-tyyppinen application/x-iso9660-image.

## ISO-tiedostomuoto

ISO-tiedostomuoto ei ole kuin muut säilötiedostomuodot, vaikka se arkistoi määritetyn sisällön sisällön. Arkisto luodaan binääritiedostona, jossa on sisällön ja tiedostojärjestelmän tietojen tarkka rakenne. ISO-tiedostomuoto kuvataan {{HYPERLINKKI}}:ssa seuraavasti.

### ISO-tiedoston ylätason rakenne

Tiedoston yleinen rakenne koostuu:

 * Järjestelmäalue - 32 768 tavua ja ISO_9660 ei käytä sitä
 * Data Area - koostuu volyymikuvausjoukosta ja polkutaulukoista, hakemistoista ja tiedostoista

### Volume Descriptor Set

Tietoalue alkaa tilavuuskuvausjoukolla, yhden tai useamman tilavuuskuvaajan joukolla, joka päättyy tilavuuskuvausjoukon päätteellä. Nämä yhdessä toimivat tietoalueen otsikkona ja kuvaavat sen sisältöä (samanlainen kuin BIOS-parametrilohko, jota FAT-, HPFS- ja NTFS-alustetut levyt käyttävät).

Tilavuuskuvaajajoukko on alla olevan kuvan mukainen.

|Volume Descriptor Set|
---|
|Välimäärän kuvaaja #1|
|...|
|Välimäärän kuvaaja #N|
|Volume deskriptor set terminator|

#### Volume Descriptor

Jokainen tilavuuskuvaaja on kooltaan 2048 tavua ja sillä on seuraava rakenne:

|Osa |Tyyppi |Tunnus |Versio |Data|
---|---|---|---|---|
|Koko |1 tavu |5 tavua (aina 'CD001') |1 tavu (aina 0x01) |2 041 tavua|

## Viitteet

* [Optisen levyn kuva - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Tiedostojen allekirjoitukset](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)


