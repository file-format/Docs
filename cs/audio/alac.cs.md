---
date: 2021-03-21
keywords: alac, formát souboru alac, přípona .alac
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o formátu souboru ALAC a rozhraních API, která mohou vytvářet a otevírat soubory ALAC."
title: ALAC - formát souboru Apple Lossless Audio Codec
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Co je soubor ALAC?

Formát souboru ALAC je Apple Lossless Audio Codec (ALAC), který používá kontejner QuickTime vyhovující MPEG-4. Byl představen v roce 2004 jako proprietární formát souborů, až do roku 2011, kdy jej Apple zpřístupnil jako open source a bez licenčních poplatků. Formát je podobný [FLAC](/cs/audio/flac/) (Free Lossless Audio Codec), ale nabízí srovnatelně vyšší kompresi. Nabízí lépe znějící alternativu k [AAC](/cs/audio/aac/) nebo [MP3](/cs/audio/mp3/). Zvukové soubory kódované kodekem ALAC lze otevřít pomocí Apple QuickTime, Apple iTunes a Microsoft Windows Media Player s kodekem K-Lite.

## Formát souboru ALAC

Soubory založené na kodeku ALAC jsou binární soubory, které jsou k dispozici jako [otevřený zdroj na GitHubu](https://github.com/macosforge/alac) pro vývojáře. Obsahuje zdroje pro kodér a dekodér ALAC. Apple také poskytl nástroj příkazového řádku, nazvaný `alacconvert`, pro čtení a zápis zvukových dat do/ze souborů Core Audio Format (CAF) a [WAVE](/cs/audio/wav/). Následuje několik klíčových bodů o formátu souboru ALAC.

1. "Bitové hloubky" - 16, 20, 24 a 32 bitů.
1. "Vzorkovací frekvence" - Libovolná vzorkovací frekvence celého čísla od 1 do 384 000 Hz. Mohou být podporovány teoretické frekvence až 4 294 967 295 (2^32 - 1) Hz.
1. `Packet Size` - Výchozí velikost paketu je výchozí 4096 ukázkových snímků zvuku na paket. Jiné velikosti balení jsou jistě možné. Není však zaručeno, že velikosti paketů, které nejsou výchozí, budou správně fungovat na všech hardwarových zařízeních, která podporují Apple Lossless. Pakety nad 16 384 ukázkových snímků nejsou podporovány.
1. `Podporované kanály` - Podporuje jeden až osm kanálů. Každý kanál má následující pořadí informací.

|Num Chan| Objednávka|
|---|---|
|1 |mono|
|2 |stereo (levý, pravý)|
|3 |MPEG 3.0 B (střed, levý, pravý)|
|4 |MPEG 4.0 B (střed, levý, pravý, středový prostorový zvuk)|
|5 |MPEG 5.0 D (střed, levý, pravý, levý prostorový, pravý prostorový)|
|6 |MPEG 5.1 D (střed, levý, pravý, levý prostorový, pravý prostorový, nízkofrekvenční efekty)|
|7 |Apple AAC 6.1 (střed, levý, pravý, levý prostorový, pravý prostorový, středový prostorový, nízkofrekvenční efekty)|
|8 |MPEG 7.1 B (střed, levý střed, pravý střed, levý, pravý, levý prostorový, pravý prostorový, nízkofrekvenční efekty)|

## Reference

* [ALAC – Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac na GitHubu](https://github.com/macosforge/alac)

