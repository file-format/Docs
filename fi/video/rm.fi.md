---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaita RM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RM-tiedostons.
title: RM tiedostolomakeat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Mikä on RM-tiedosto? ##

RealMedia on RealNetworksin kehittämä multimediasäilömuoto, joka käyttää .rm-laajennusta. Sitä käytetään yhdistelmän [RealAudio (RA)](/audio/ra/) ja [RealVideo(RV)](/video/rv/) kanssa suoratoistoon Internetin kautta. Näiden virtojen bittinopeus on vakio. RealNetworks kehitti muuttuvaa bittinopeutta varten RealMedia Variable Bitrate (RMVB) -muodon. RealMedia soveltuu sisällön suoratoistoon Internetin kautta ja sitä voidaan käyttää esimerkiksi suoran television suoratoistoon.

## RealMedia-tiedoston ## rakenne

RealMedia-tiedosto koostuu sarjasta paloja, joista jokaisella on seuraava rakenne:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Seuraavat ovat RealMedia-tiedostossa olevat palotyypit:

- **RealMedia-tiedoston otsikko (.RMF)**: Tämän on oltava RealMedia-tiedoston ensimmäinen osa. Yhdessä tiedostossa on vain yksi RMF-pala. Se sisältää tietoa otsikoiden määrästä.
- **Tiedoston ominaisuuksien otsikko (PROP)**: Tämä sisältää tietoja RealMedia-tiedoston yleisistä ominaisuuksista. Jokaisessa RealMedia-tiedostossa on vain yksi tämäntyyppinen pala.
- **Media-ominaisuuksien otsikko (MDPR)**: Tämä osa sisältää tietoja virran ominaisuuksista. Se sisältää tietoja streamin tyypistä ja käytetystä koodekista. Jokaiselle tiedoston streamille on yksi MDPR-kappale.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Data header (DATA)**: Tämä osa sisältää ryhmän datapaketteja.
- **Hakemistootsikko (INDX)**: Tämä osa tulee kaikkien DATA-osien jälkeen ja sisältää hakemistomerkintöjä. Yhdessä tiedostossa voi olla enemmän kuin yksi INDX-pala.

## Tuetut ääni- ja videomuodot ##

### Ääniformaatit ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- kokki: kokki
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- Raac: LC-AAC
- racp: HE-AAC

### Videoformaatit ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264-prekursori
- RV40: H.264 prekursori, RV40
- RVTR: H.263+ (RV20)

## Viitteet ##

- {{HYPERLINKKI}}

