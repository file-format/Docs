---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltienaa VOB-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata VOB-tiedostons.
title: VOB-tiedostolomakeat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Mikä on VOB-tiedosto? ##

VOB-tiedostot tallennetaan tyypillisesti VIDEO_TS-hakemistoon DVD-levyllä, jonka tunniste on .vob. VOB-tiedostot sisältävät video- ja äänidataa sekä muita tietoja, kuten valikoita ja tekstityksiä. VOB perustuu MPEG-2-ohjelmavirtamuotoon, mutta sillä on lisärajoituksia ja -määrityksiä yksityisille virroille. VOB-tiedostot ovat tiukka osajoukko MPEG-ohjelmavirroista, joten kaikki VOB-tiedostot ovat MPEG-ohjelmavirtoja, mutta kaikki MPEG-ohjelmavirrat eivät ole VOB-yhteensopivia.

## DVD-videon rakenne ##

Kun DVD-levy avataan tietokoneessa, VIDEO_TS on ylimmän tason hakemisto, jossa on AUDIO_TS. AUDIO_TS on tyhjä eikä sitä käytetä. VIDEO_TS-hakemiston sisällä on VOB-, BUP- ja IFO-tiedostoja. VOB-tiedostot sisältävät MPEG-sisällön. Ne on jaettu enintään 1 Gt:n osiin, jotta ne ovat yhteensopivia kaikkien käyttöjärjestelmien kanssa. IFO-tiedostot sisältävät tietoa valikoista ja otsikkorakenteesta. BUK-tiedostot ovat samannimistä IFO-tiedostojen varmuuskopioita. Nämä tiedostot on tarkoitettu säilytettäväksi erillään fyysisesti, jotta jos IFO-tiedosto vaurioituu DVD-levyn fyysisen vaurion vuoksi, BUK-tiedosto voi tarjota samat tiedot.

### Fyysinen ulkoasu ###

- Kaikkien levyllä olevien tiedostojen on oltava vierekkäisiä.
- Asiaan liittyvien tiedostojen tulee olla vierekkäin (VOB, IFO, BUP).
- Numeroitujen tiedostojen tulee olla nousevassa järjestyksessä.

## kopiosuojaus ##

Monet video-DVD-levyt ovat salattuja ja estävät tietojen kopioimisen DVD-levyltä. Todennus- ja salauksenpurkuavaimia tarvitaan niiden tiedostojen toistamiseen, jotka sijaitsevat DVD-levyn saavuttamattomalla aloitusalueella. Näitä avaimia käyttää DVD-soittimessa tai ohjelmistosoittimessa oleva CSS-salauksenpurkuohjelmisto. Ilman näppäimiä videotiedostoja ei voida toistaa, koska näppäimiä pyydetään, kun tiedostoja avataan.

## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}

