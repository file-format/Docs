---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltienaa SRT-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata SRT-tiedostons.
title: SRT-tiedostolomakeat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Mikä on SRT-tiedosto? ##

SRT (SubRip-tiedostomuoto) on yksinkertainen tekstitystiedosto, joka on tallennettu SubRip-tiedostomuotoon .srt-tunnisteella. Se sisältää peräkkäisen määrän tekstityksiä, aloitus- ja lopetusaikaleimat sekä tekstitystekstiä. SRT-tiedostot mahdollistavat tekstityksen lisäämisen videosisältöön sen valmistuksen jälkeen.

## SRT-tiedostorakenne ##

Jokaisessa tekstityksessä on neljä osaa SRT-tiedostossa.

1. Numeerinen laskuri, joka osoittaa tekstityksen numeron tai sijainnin.
1. Tekstityksen alkamis- ja päättymisaika erotettuna --> merkeillä
1. Tekstitys yhdellä tai useammalla rivillä.
1. Tyhjä rivi, joka osoittaa tekstityksen lopun.

### Esimerkki SRT:stä ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Ajan määrittämiseen käytetään muotoa *tunnit:minuutit:sekunnit,millisekuntit (00:00:00,000)*.

## SRT-tiedostojen muotoilu ##

SRT-tiedostojen muotoilu on johdettu HTML-tunnisteista. SRT-tiedoston muotoilutunnisteet on lueteltu alla.

| Vaikutus | Tunnisteet |
| --- | --- |
|Lihavointi|**\ <b>...\</b> ** tai {b}...{/b}|
|Kursivoitu|**\ <i>...\</i> ** tai **{i}...{/i}**|
|Alleviivaus|**\ <u>...\</u> ** tai **{u}...{/u}**|
|Fontin väri|**\ <font color=white>...\</font> **|
|Line Position|**{\a3}** (osoittaa, että tekstin pitäisi alkaa näkyä rivillä 3)

## SubRip-ohjelmisto ##

SubRip on ilmainen ohjelmisto, joka toimii Windowsissa. Se poimii tekstitykset ja niiden ajoitukset eri videoformaateista ja tallentaa tekstitykset SRT-muotoon. SubRip käyttää optista merkintunnistusta tekstityksen poimimiseen live-videosta, muista videotiedostoista ja DVD-levyistä.

## Viitteet ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
