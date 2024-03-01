---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaitse MP4-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata MP4-tiedostojas.
title: MP4-tiedostolomakeat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Mikä on MP4-tiedosto? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Lyhyt historia ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. MP4:n ensimmäinen versio (ISO/IEC 14496-1:2001) oli vuonna 1999 julkaistun MPEG-4 Part 1: Systems -määrittelyn versio. MP4-tiedostomuoto yleistettiin ISO Base Media File Format -standardiin ISO/IEC 14496-12. :2004, joka määritteli aikaperusteisten mediatiedostojen yleisen rakenteen. Tämän seurauksena sitä käytetään muiden tiedostomuotojen perustana.

## MP4-tiedostojen rakenne ##

MP4 on laajennettava säilötiedosto, mikä tarkoittaa, että se ei määrittele tiukkaa rakennetta ja sallii mukautetun rakenteen ja hierarkian jokaiselle mediatyypille. MP4-tiedoston tiedot on jaettu kahteen osaan, joista ensimmäinen sisältää mediaan liittyvät tiedot ja toinen metatiedot. Mediatiedot sisältävät ääntä tai videota, ja metatiedot osoittavat satunnaiskäytön liput, aikaleimat jne.
MP4:n rakenteita kutsutaan tyypillisesti atomeiksi tai laatikoiksi. Atomin vähimmäiskoko on 8 tavua (ensimmäiset 4 tavua määrittelevät koon ja seuraavat 4 tavua tyypin). Tässä on luettelo MP-tiedostojen juuritason atomeista:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: Sisältää progressiivisen videon lataus-/lataustiedot.
- **moov**: säilö kaikille elokuvan metatiedoille.
- **moof**: Säiliö, jossa on videopätkiä.
- **mfra**: Säilö, jolla on satunnainen pääsy videon fragmenttiin
- **mdat**: Median tietosäiliö.
- **stts**: näyte-aikataulukko.
- **stsc**: näyte-palataulukko.
- **stsz**: näytekoot (kehystys)
- **meta**: Säilö, jossa on metatietotiedot.

Tässä on luettelo MP4:ssä käytetyistä toisen tason atomeista:

- **mvhd**: Sisältää videon otsikkotiedot ja kaikki videon tiedot.
- **trak**: Säiliö yksittäisellä radalla.
- **udta**: Säilö, jossa on käyttäjä- ja kappaletiedot.
- **jodit**: MP4-tiedoston kuvaus

## Viitteet ##

- {{HYPERLINKKI1}}

