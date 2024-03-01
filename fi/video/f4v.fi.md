---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaitse F4V-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata F4V-tiedostones
title: F4V tiedostolomakeat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Mikä on F4V-tiedosto? ##

F4V (Flash MP4 Video File) on videotiedosto, joka on tallennettu .f4v-tunnisteella. Se perustuu ISO-perusmediatiedostomuotoon (MPEG-4, osa 12). Se on hyvin samanlainen kuin {{HYPERLINKKI}}, minkä vuoksi sitä kutsutaan epävirallisesti myös Flash MP4:ksi. [FLV](/video/flv/):lla oli rajoituksia H.264/ACC-sisällön suoratoistossa, minkä vuoksi Adobe Systems loi uuden F4V-muodon. Flash Player voi toistaa F4V-tiedostoja Flash Player 9 -päivityksen 3 julkaisun jälkeen.

## F4V-tiedostojen rakenne ##

F4V-tiedostomuoto perustuu ISO-perusmediatiedostomuotoon (MPEG-4, osa 12) ja on hyvin samanlainen kuin MP4-muoto. Lisätietoja rakenteesta on {{HYPERLINKKI}}-sivulla. Suurin ero F4V:n ja MP4:n välillä on metatietomuodot, jotka F4V voi tallentaa. Alla on luettelo F4V-muodon tukemista metatietomuodoista.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP-metatietolaatikko**: Tämä laatikko tulee heti Movie (moov) -ruudun jälkeen. Tämän avulla tiedosto voi välittää XMP-metatiedot SWF-elokuvaan ActionScriptin kautta.
- **ilst box**: Tämä laatikko sijaitsee Meta (meta) -ruudun sisällä ja voi sisältää useita metatietotageja. Tuetut tietotyypit on lueteltu alla.
  - "**0**: mukautetut tiedot."
  - "**1**: Tekstitiedot."
  - "**12, 14**: Binaaridata"
  - "**21**: Yleiset tiedot."
- **Tekstiraidan metatietolaatikko**: Tekstiesimerkit (teksti tai tx3g) Media Databoxin (mdat) sisällä. Se voi sisältää seuraavat metatietoruudut.
  - "**Tyylilaatikko**: Tekstin tyylin tiedot."
  - "**Korostusruutu**: Määrittää korostettavan tekstin alueen."
  - "**Korostusvärilaatikko**: Määrittää tekstin korostuksen värin."
  - "**Karaokeboksi**: Määritti karaoken metatiedot."
  - "**Scroll Delay box**: Määrittää vieritysviiveen."
  - "**Drop Shadow Offset -ruutu**: Määrittää tekstin varjon siirtymän koordinaatit."
  - "**Drop Shadow Alpha -ruutu**: Määrittää tekstin varjon alfa-arvon."
  - "**Hypertekstilaatikko**: Määrittää hypertekstin ja vaihtoehtoisen tekstin tekstialueella."
  - "**Tekstilaatikko**: Määrittää tekstilaatikon koordinaatit."
  - "**Vilkkuva laatikko**: Määrittää vilkkumisen tekstialueelle."
  - "**Tekstin rivityslaatikko**: Asettaa tekstin rivityslipun."
  - "**Tekstin rivityslaatikko**: Asettaa tekstin rivityslipun."

## Viitteet ##

- {{HYPERLINKKI1}}

