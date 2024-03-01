---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaita OGG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OGG-tiedostons.
title: OGG File - Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Mikä on OGG-tiedosto?

OGG on Ogg Vorbis -pakattu äänitiedosto, joka tallennetaan .ogg-tunnisteella. OGG-tiedostoja käytetään äänidatan tallentamiseen, ja ne voivat sisältää myös artisti- ja kappaletietoja ja metatietoja. OGG on ilmainen ja avoin konttimuoto, jota ylläpitää Xiph.Org Foundation.

## OGG-tiedostomuodon lyhyt historia

Ogg-projekti aloitettiin osana suurempaa projektia vuonna 1993 ja se sai nimekseen Squish, mutta olemassa olevan tavaramerkin vuoksi se nimettiin uudelleen OggSquishiksi. Sitä kuvailtiin yritykseksi luoda joustava pakattu äänimuoto nykyaikaisia äänisovelluksia varten. OGG-viite erotettiin Vorbisista 2. syyskuuta 2000.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. 30. kesäkuuta 2009 mennessä OGG oli ainoa säilömuoto, jota Firefox 3.5:n HTML5-toteutus tukee.

## OGG tiedostomuoto

OGG-muoto koostuu tietopaloista. Jokaista osaa kutsutaan Ogg-sivuksi. Jokainen sivu alkaa kirjaimella OggS, joka tunnistaa Ogg-muodon. Otsikko sisältää sarjanumeron ja sivunumeron, joka tunnistaa jokaisen sivun osaksi sarjaa. Sivu koostuu seuraavista osista.

- **Sivun otsikko**
  - "**Capture Pattern (32 bits)**: Tätä käytetään synkronointiin jäsennettäessä OGG-tiedostoja."
  - "**Versio(8 bittiä)**: Osoittaa Ogg-bittivirran version."
  - "**Otsikkotyyppi (8 bittiä)**: Se ilmaisee sivun tyypin."

| Bittinen | Arvo | Kuvaus |
| --- | --- | --- |
| 0 | 0x01 | Osoittaa, että sivun ensimmäinen paketti on jatkoa loogisen bittivirran edelliselle paketille. |
| 1 | 0x02 | Osoittaa, että tämä sivu on ensimmäinen loogisessa bittivirrassa. |
| 2 | 0x04 | Osoittaa, että tämä sivu on loogisen bittivirran viimeinen. |

  - "**Rakeen sijainti (64 bittiä)**: Se on aikamerkki, jonka merkityksen määrittää koodekki."
  - "**Bittivirran sarjanumero (32 bittiä)**: Se on sarjanumero, joka tunnistaa tiettyyn loogiseen bittivirtaan kuuluvan sivun."
  - "**Sivun järjestysnumero (32 bittiä)**: Se ilmaisee sen sivun järjestyksen, jonka ensimmäinen sivu alkaa nollasta."
  - "**Tarkistussumma(32 bittiä)**: Tarjoaa CRC32-tarkistussumman koko sivutiedosta."
  - "**Sivun segmentit (8 bittiä)**: Ilmaisee sivulla olevien segmenttien määrän."
  - "**Segmenttitaulukko**: Se on 8-bittisten arvojen joukko, joka ilmaisee sivun rungon kunkin segmentin pituuden."
- **Metatiedot**: VorbisComment on laajimmin tuettu mekanismi metatietojen tallentamiseen. Muita mekanismeja ovat seuraavat:
  - "FLAC-metatietolohkot"
  - "Oggin luuranko"
  - "Jatkuva median merkintäkieli"

## Viitteet ##

- {{HYPERLINKKI1}}

