---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaita FLV-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata FLV-tiedostons.
title: FLV-tiedostolomakeat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Mikä on FLV-tiedosto? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe-järjestelmät loivat F4V:n vuonna 2007 FLV:n rajoitusten vuoksi.

### Koodaus ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. Flash Player -tuen versio 8 On2 TrueMotion VP6 -videobittivirroille. Se on suositeltu pakkausmuoto Flash Player 8:lle ja uudemmille. FLV tukee ääntä MP3-muodossa, Nellymoser Asao Codec ja avoimen lähdekoodin Speex-koodekki. Se tukee myös pakkaamatonta ääntä tai ADPCM-muotoista ääntä. Flash Player 9:n uusimmat versiot tukevat AAC:tä (HE-AAC/AAC SBR, AAC Main Profile ja AAC-LC).

## Rakenne ##

FLV-tiedostot koostuvat otsikoista ja paketeista. FLV-tiedosto alkaa otsikolla. Otsikossa on seuraavat kentät.

- **Allekirjoitus**: Sen arvo on FLV
- **Version**: Its default value is 1. Vain 0x01 on kelvollinen.
- **Liput**: 0x04 käytetään äänelle ja 0x01 käytetään videolle, joten 0x05 käytetään sekä äänelle että videolle.
- **Header Size**: The default value is 9. Sitä käytetään ohittamaan uudempi laajennettu otsikko.

Otsikon jälkeen tulee Paketit. FLV-tiedosto on jaettu useiksi paketeiksi, joita kutsutaan FLV-tunnisteiksi ja joissa on 15-tavuiset otsikot. Paketit sisältävät äänen, videon, skriptien, salaustietojen ja hyötykuorman metatiedot. FLV-paketeissa on seuraavat kentät.

- **Varattu**: Se on varattu FMS:lle ja sen pitäisi olla 0.
- **Suodatin**: Osoittaa, onko paketit suodatettu vai ei.
  - "**0**: Esikäsittelyä ei vaadita. Tätä käytetään salaamattomille tiedostoille."
  - "**1**: Esikäsittely vaaditaan. Tätä käytetään salatuille tiedostoille"
- **Pakettityyppi**: Tämä määrittää paketin sisällön tyypin.
  - "**8**: Ääni"
  - "**9**: Video"
  - "**18**: Käsikirjoitustiedot"
- **Tiedon koko**: Tämä ilmaisee viestin pituuden.
- **Aikaleima pienempi**: Tämä tallentaa aikaleiman millisekunteina, jolloin tunnistetiedot ovat voimassa. Ensimmäisen paketin arvoksi on asetettu NULL.
- **Timestamp Upper**: Laajennus uint32_be-arvon luomiseksi.
- **Stream ID**: Tämä on asetettu arvoon NULL ensimmäiselle streamille.
- **Payload Data**: Tämä data perustuu pakettityyppiin.

## Viitteet ##

- {{HYPERLINKKI1}}

