{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MXF - Materiaalinvaihtomuoto",
  "keywords": [
"MXF",
"matroska video",
"mkv muodossa",
"kuinka toistaa MXF-tiedostoja",
"SMPTE",
"multimedia",
"video"
],
  "description": "Opi MXF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MXF-tiedostoja.",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mx-fif"
}
},
  "lastmod": "2021-03-01"
}

## Mikä on MXF-tiedosto?

Tiedosto, jonka tarkenne on .mxf, on multimediasäilömuoto, joka sisältää digitaalista video- ja äänimediaa sekä tiedoston metatietoja. Se noudattaa SMPTE-standardia (Society of Motion Picture and Television Engineers), joka on maailmanlaajuinen järjestö, joka koostuu insinööri-, teknologia- ja media- ja viihdeteollisuudessa työskentelevistä johtajista. MXF-tiedostot voidaan muuntaa muihin tiedostomuotoihin, kuten [AVI](/video/avi/) tai [MOV](/video/mov/).

## MXF tiedostomuoto

MXF-tiedostot ovat itse asiassa binääritiedostoja, jotka koostuvat tavusarjasta tietyssä muodossa. Dekoodaussovellusten on oltava tämän muodon mukaisia, jotta se voi ymmärtää ja poimia siitä tietoa. Muoto mahdollistaa uusien kohteiden lisäämisen rikkomatta taaksepäin yhteensopivuutta käyttämällä KLV-koodausta, joka on kuvattu alla.

 * Avain – elementin tunniste, SMPTE Universal Label (UL)
 * Pituus – datan pituus, joka on vaihtuvapituinen koodaus, jota käytetään tämän kohteen vaatiman tilan vähentämiseksi
 * Arvo – elementin todellinen arvo.

### SMPTE-muodon tekniset tiedot

MXF-tiedostomuoto on määritetty seuraavien SMPTE-määritysten mukaan.

* SMPTE ST 377-1:2011. Televisio — Materiaalinvaihtomuoto (MXF) — Tiedostomuodon määritykset

* SMPTE ST 377-2 (työ käynnissä tammikuusta 2012). KLV-koodattu laajennussyntaksi MXF:lle.

* SMPTE ST 378:2004 (arkistoitu 2010). Televisio — Materiaalinvaihtoformaatti (MXF) — Toimintamalli 1a (yksittäinen tuote, yksi paketti)

* SMPTE ST 379-1:2009. Materiaalinvaihtoformaatti (MXF) — MXF Generic Container

* SMPTE ST 379-2:2010. Materiaalinvaihtomuoto (MXF) – MXF-rajoitettu yleinen säiliö

* SMPTE ST 380:2004. Televisio — Materiaalinvaihtoformaatti (MXF) — Kuvaileva metatietojärjestelmä 1 (standardi, dynaaminen)

* SMPTE ST 381-1:2005. Televisio — Materiaalinvaihtomuoto (MXF) — MPEG-virtojen yhdistäminen MXF:n yleiseen säilöön (dynaaminen)

* SMPTE ST 381-2:2011. Materiaalinvaihtoformaatti (MXF) — MPEG-virtojen yhdistäminen MXF-rajoitettuun yleiseen säilöön

* SMPTE ST 382:2007. Materiaalinvaihtomuoto (MXF) — AES3-virtojen ja Broadcast Wave Audion yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 383:2008. Televisio — Materiaalinvaihtoformaatti (MXF) — DV-DIF-tietojen yhdistäminen yleiseen MXF-säilöön

* SMPTE ST 384:2005. Televisio — Materiaalinvaihtoformaatti (MXF) — Pakkaamattomien kuvien yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 385:2004. Televisio — Materiaalinvaihtomuoto (MXF) — SDTI-CP Essencen ja metatietojen yhdistäminen yleiseen MXF-säilöön

* SMPTE ST 386:2004 (arkistoitu 2010). Televisio — Materiaalinvaihtoformaatti (MXF) — Tyypin D-10 Essence -tietojen yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 387:2004 (arkistoitu 2010). Televisio — Materiaalinvaihtoformaatti (MXF) — Tyypin D-11 Essence-tietojen yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 388:2004 (arkistoitu 2010). Televisio — Materiaalinvaihtoformaatti (MXF) — A-lain koodatun äänen yhdistäminen MXF:n yleiseen säilöön

* SMPTE ST 389:2005. Televisio — Materiaalinvaihtoformaatti (MXF) — MXF Generic Container Reverse Play System Element

* SMPTE ST 390:2011. Televisio — Materiaalinvaihtoformaatti (MXF) — Erikoistettu toimintamalli "Atom" (yksittäisen kohteen yksinkertaistettu esitys)

* SMPTE ST 391:2004 (arkistoitu 2010). Televisio — Materiaalinvaihtoformaatti (MXF) — Toimintamalli 1b (yksittäinen tuote, ryhmittyneet paketit)

* SMPTE ST 392:2004. Televisio — Materiaalinvaihtoformaatti (MXF) — Toimintamalli 2a (soittolistan kohteet, yksittäinen paketti)

* SMPTE ST 393:2004. Televisio — Materiaalinvaihtoformaatti (MXF) — Toimintamalli 2b (soittolistan kohteet, ryhmäpaketit)

* SMPTE ST 394:2006. Televisio — Materiaalinvaihtoformaatti (MXF) — Järjestelmäkaavio 1 yleiselle MXF-säiliölle

* SMPTE ST 405:2006. Televisio — Materiaalinvaihtoformaatti (MXF) — Elementit ja yksittäiset tietokohteet yleiselle MXF-säiliöjärjestelmälle 1

* SMPTE ST 407:2006. Televisio — MXF — Toimintamallit 3a ja 3b

* SMPTE ST 408:2006. Televisio — MXF — Toimintamallit 1c, 2c ja 3c

* SMPTE ST 410: 2008. Materiaalinvaihtomuoto - yleinen virranosio.

* SMPTE ST 422:2006. Materiaalinvaihtomuoto — JPEG2000-koodivirtojen yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000 -sovellus

* SMPTE ST 429.5:2006. D-Cinema Packaging — ajastettu tekstiraitatiedosto

* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption

* SMPTE ST 434:2006. Materiaalin vaihtomuoto — XML-koodaus metatiedoille ja tiedostorakennetiedoille

* SMPTE ST 436:2006. Televisio — MXF-kartoitukset VBI-linjoille ja aputietopaketteille

* SMPTE ST 2019-4:2009. VC-3-koodausyksiköiden yhdistäminen yleiseen MXF-säiliöön

* SMPTE ST 2037:2009. VC-1:n yhdistäminen MXF Generic Containeriin

* SMPTE RP 2008:2008. Materiaalinvaihtomuoto — AVC-virtojen yhdistäminen MXF:n yleiseen säilöön

* SMPTE RP 2057:2011. Tekstipohjainen metatietojen kuljetus MXF:ssä

* SMPTE EG 41:2004. Materiaalinvaihtoformaatti (MXF) — Tekninen ohje. Huomautus: Tätä asiakirjaa ei enää lueteltu SMPTE-verkkosivustolla, kun sitä käytiin tammikuussa 2012.

* SMPTE EG 42:2004. Materiaalinvaihtomuoto (MXF) — MXF Descriptive Metadata

* SMPTE RDD 3:2008. e-VTR MXF -yhteentoimivuusmääritys

* SMPTE RDD 9-2009. Sony MPEG Long GOP -tuotteiden MXF-yhteensopivuusmääritys

* SMPTE metatietorekisterin taulukkolaskentavalikko.


### MXF:n rakenteelliset metatiedot

Rakenteelliset metatiedot ovat tärkeitä MXF-tiedostossa, koska ne sisältävät hyödyllistä tietoa tiedoston sisällöstä. MXF-metatiedot sisältävät tietoja, kuten kuvanopeuden, kehyskoon, tiedoston luontipäivämäärän ja mukautetun muokkauspäivämäärän. Rakenteelliset metatiedot kuvaavat MXF-tiedoston rakennetta ja ominaisuuksia, jotka sisältävät eri olennaisten komponenttien teknisen kuvauksen ja tulosten aikajanan muodostamisen.

## Viitteet

 * [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [Avoimen lähdekoodin C++ -kirjasto MXF:lle](http://www.freemxf.org/)

