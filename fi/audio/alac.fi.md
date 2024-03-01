---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lansaita ALAC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ALAC-tiedostons.
title: ALAC - Apple Lossless Audio Codec -tiedostolomakeat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Mikä on ALAC-tiedosto?

ALAC-tiedostomuoto on Apple Lossless Audio Codec (ALAC), joka käyttää MPEG-4-yhteensopivaa QuickTime-säilöä. Se esiteltiin vuonna 2004 patentoiduna tiedostomuotona vuoteen 2011 asti, jolloin Apple julkaisi sen avoimen lähdekoodin ja rojaltivapaana. Muoto on samanlainen kuin [FLAC](/audio/flac/) (Free Lossless Audio Codec), mutta tarjoaa enemmän pakkausta verrattuna. Se tarjoaa paremman kuuloisen vaihtoehdon kuin [AAC](/audio/aac/) tai [MP3](/audio/mp3/). ALAC-koodekilla koodattuja äänitiedostoja voidaan avata Apple QuickTimella, Apple iTunesilla ja Micrsoft Windows Media Playerilla K-Lite-koodekilla.

## ALAC-tiedostomuoto

ALAC-koodekkiin perustuvat tiedostot ovat binääritiedostoja, jotka ovat saatavilla nimellä [open source on GitHub](https://github.com/macosforge/alac) kehittäjien viitteeksi. Se sisältää lähteet ALAC-kooderille ja dekooderille. Apple on myös toimittanut komentorivityökalun nimeltä alacconvert, jonka avulla voit lukea ja kirjoittaa äänidatan Core Audio Format (CAF)- ja [WAVE](/audio/wav/)-tiedostoihin tai niistä. Seuraavassa on joitain keskeisiä kohtia ALAC-tiedostomuodosta.

 1. Bittisyvyydet - 16, 20, 24 ja 32 bittiä.
 1. Sample Rate - Mikä tahansa mielivaltainen kokonaislukunäytetaajuus 1 - 384 000 Hz. Teoreettisia nopeuksia jopa 4 294 967 295 (2^32 - 1) Hz voidaan tukea.
 1. Paketin koko - Paketin oletuskoko on 4096 näytekehystä ääntä pakettia kohden. Muut pakettikoot ovat varmasti mahdollisia. Ei kuitenkaan ole taattu, että muut kuin oletusarvoiset pakettikoot toimisivat oikein kaikissa Apple Lossless -laitteita tukevissa laitteissa. Yli 16 384 näytekehyksen paketteja ei tueta.
 1. Tuetut kanavat - Se tukee yhdestä kahdeksaan kanavaa. Jokaisella kanavalla on seuraava tietojärjestys.

|Num Chan| Tilaa|
|---|---|
|1 |mono|
|2 |stereo (vasen, oikea)|
|3 |MPEG 3.0 B (keskellä, vasen, oikea)|
|4 |MPEG 4.0 B (keski, vasen, oikea, keskitila)|
|5 |MPEG 5.0 D (keski, vasen, oikea, vasen surround, oikea surround)|
|6 |MPEG 5.1 D (keski, vasen, oikea, vasen surround, oikea surround, matalataajuiset tehosteet)|
|7 |Apple AAC 6.1 (keski, vasen, oikea, vasen surround, oikea surround, keskisurround, matalataajuiset tehosteet)|
|8 |MPEG 7.1 B (Keski, Vasen Keski, Oikea Keski, Vasen, Oikea, Vasen Surround, Oikea Surround, Matalataajuiset tehosteet)|

## Viitteet

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)

* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)

* [macosforge - alac GitHubissa](https://github.com/macosforge/alac)


