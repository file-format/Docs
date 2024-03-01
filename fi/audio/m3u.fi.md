---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaitse noin M3U-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata M3U-tiedostons.
title: M3U tiedostolomakeat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Mikä on M3U-tiedosto? ##

M3U (MP3 URL) on äänisoittolistatiedosto, joka on tallennettu .m3u-tunnisteella. M3U ei ole varsinainen äänitiedosto, se vain osoittaa ääni- ja joskus videotiedostoja. Fraunhofer on kehittänyt M3U:n käytettäväksi Winplay3-ohjelmiston kanssa. Sitä tukevat myös erilaiset mediasoittimet ja ohjelmistot.

## M3U tiedostomuoto

M3U-tiedostomuodolle ei ole virallista määritystä, se on tosiasiallinen standardi. M3U on pelkkä tekstitiedosto, joka käyttää .m3u-tunnistetta, jos teksti on koodattu paikallisen järjestelmän oletusarvoisella ei-Unicode-koodauksella, tai .m3u8-tunnisteella, jos teksti on UTF-8-koodattu. Jokainen M3U-tiedoston merkintä voi olla jokin seuraavista:

- Tiedoston absoluuttinen polku
- Tiedostopolku suhteessa M3U-tiedostoon.
- URL

### Laajennettu M3U ###

Laajennetussa M3U:ssa on lisäohjeita, jotka alkavat #:lla ja päättyvät kaksoispisteeseen (:), jos niillä on parametreja. Alla on luettelo laajennetun M3U:n direktiiveistä.

- **#EXTM3U** - Se on tiedoston otsikko, joka ilmaisee Extended M3U:n, ja sen on oltava tiedoston ensimmäinen rivi.
- **#EXTENC:** - Tekstin koodaus. Sen on oltava tiedoston 2. rivi.
- **#EXTINF:** - Käytetään kappaletietoihin ja muihin lisäominaisuuksiin.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Aloita nimien ryhmittely
- **#EXTALB:** - Albumin tiedot
- **#EXTART:** - Albumin artisti
- **#EXTGENRE** - Albumin tyylilaji
- **#EXTM3A** - Yhden tiedoston soittolista albumin kappaleille tai jaksoille.
- **#EXTBYT:** - Tiedoston koko tavuina.
- **#EXTBIN:** - Seuraavassa on binaaridata.
- **#EXTIMG:** - Logo, kansi tai muut kuvat.

### HLS M3U ###

Apple loi HLS:n (HTTP Live Streaming) äänen ja radion suoratoistoon iOS-laitteisiin. Se perustuu UTF-8-koodattuun laajennettuun M3U:han. IETF standardoi sen nimellä RFC 8216 vuonna 2017. HLS-soittolistan tagit alkavat #EXT-X-. Alla on luettelo HLS-tunnisteista

- **EXT-X-VERSION** - Ilmaisee tiedoston yhteensopivuusversion median ja sen palvelimen perusteella.
- **#EXT-X-START:** - Ilmaisee soittolistan ensisijaisen aloituskohdan.
- **#EXT-X-PLAYLIST-TYPE:** - Tarjoaa soittolistan tyypin (TAPAHTUMA tai VOD).
- **#EXT-X-TARGETDURATION:** - Se määrittää segmentin enimmäiskeston.
- **#EXT-X-MEDIA-SEQUENCE:** - Se osoittaa median järjestysnumeron.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Se osoittaa, että kaikki medianäytteet ovat riippumattomia ja ne voidaan purkaa ilman muita segmenttejä.
- **#EXT-X-MEDIA:** - Sitä käytetään yhdistämään mediasoittolistoja, jotka sisältävät saman sisällön vaihtoehtoisia esityksiä.
- **#EXT-X-STREAM-INF:** - Se määrittää muunnelmavirran, joka on osa esityksiä.
- **#EXT-X-BYTERANGE:** - Ilmaisee, että mediasegmentti on URI-tunnisteen tunnistaman resurssin alialue.
- **#EXT-X-DISCONTINUITY** - Ilmaisee epäjatkuvuuden edellisen ja seuraavan mediasegmentin välillä.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Se mahdollistaa synkronoinnin saman Varianttivirran tai eri Varianttivirran eri esitysten välillä.
- **#EXT-X-KEY:** - Määrittää, kuinka mediasegmenttien salaus puretaan.
- **#EXT-X-MAP:** - Määrittää, kuinka Media Initialization -osio saadaan. Sovellettavat mediasegmentit on jäsennettävä.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - Se liittää tietoalueen.
- **#EXT-XI-FRAMES-ONLY** - Osoittaa, että jokainen soittolistan mediasegmentti kuvaa yhtä I-kehystä.
- **EXT-XI-FRAME-STREAM-INF** - Se osoittaa, että soittolistatiedosto sisältää multimediaesityksen I-kehykset.
- **#EXT-X-SESSION-DATA:** - Se mahdollistaa mielivaltaisten istuntotietojen lähettämisen
mukana pääsoittolistalla.
- **#EXT-X-SESSION-KEY:** - Se mahdollistaa salausavainten käytön. Asiakas voi esiladata nämä avaimet lukematta ensin soittolistaa.
- **#EXT-X-ENDLIST** - Se osoittaa, että tiedostoon ei lisätä enempää mediasegmenttejä.

Seuraava on luettelo M3U:n käyttämistä Internet-mediatyypeistä:

- **application/vnd.apple.mpegurl**: Se on M3U:n ainoa rekisteröity mediatyyppi (rekisteröity vuonna 2009), jota käytetään viittaamaan soittolistoihin HLS-sovelluksissa.
- Muut kuin HLS-sovellukset käyttävät seuraavia Internet-mediatyyppejä.
  - "**sovellus/mpegurl**"
  - "**sovellus/x-mpegurl**"
  - "**ääni/mpegurl**"
  - "**audio/x-mpegurl**"

## M3U esimerkki ##

Tämä on esimerkki M3U-tiedostosta.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

