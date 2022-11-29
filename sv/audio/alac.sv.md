---
date: 2021-03-21
keywords: alac, alac filformat, .alac extension
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig om ALAC-filformat och API:er som kan skapa och öppna ALAC-filer."
title: ALAC - Apple Lossless Audio Codec-filformat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Vad är en ALAC fil?

ALAC-filformatet är Apple Lossless Audio Codec (ALAC) som använder den MPEG-4-kompatibla QuickTime-behållaren. Det introducerades 2004 som proprietärt filformat, fram till 2011 när Apple gjorde det tillgängligt med öppen källkod och royaltyfritt. Formatet liknar [FLAC](/sv/audio/flac/) (Free Lossless Audio Codec) men erbjuder mer komprimering i jämförelse. Det erbjuder bättre ljud alternativ till [AAC](/sv/audio/aac/) eller [MP3](/sv/audio/mp3/). Ljudfiler kodade med ALAC-codec kan öppnas med Apple QuickTime, Apple iTunes och Micrsoft Windows Media Player med K-Lite-codec.

## ALAC filformat

Filer baserade på ALAC-codec är binära filer som är tillgängliga som [open source på GitHub](https://github.com/macosforge/alac) för utvecklarens referens. Den innehåller källorna för ALAC-kodaren och dekodern. Apple har också tillhandahållit ett kommandoradsverktyg, kallat `alacconvert`, för att läsa och skriva ljuddata till/från Core Audio Format (CAF) och [WAVE](/sv/audio/wav/)-filer. Följande är några viktiga punkter om ALAC-filformatet.

1. "Bitdjup" - 16, 20, 24 och 32 bitar.
1. `Sample Rate` - Alla godtyckliga heltals samplingsfrekvens från 1 till 384 000 Hz. Teoretiska hastigheter på upp till 4 294 967 295 (2^32 - 1) Hz kan stödjas.
1. `Paketstorlek` - Standardpaketstorleken är som standard 4096 ljudexempelrutor per paket. Andra paketstorlekar är säkert möjliga. Emellertid är det inte garanterat att icke-standardpaketstorlekar fungerar korrekt på alla hårdvaruenheter som stöder Apple Lossless. Paket över 16 384 exempelramar stöds inte.
1. "Supported Channels" - Den stöder en till åtta kanaler. Varje kanal har följande informationsordning.

|Num Chan| Beställ|
|---|---|
|1 |mono|
|2 |stereo (vänster, höger)|
|3 |MPEG 3.0 B (mitten, vänster, höger)|
|4 |MPEG 4.0 B (Center, Vänster, Höger, Center Surround)|
|5 |MPEG 5.0 D (Center, Vänster, Höger, Vänster Surround, Höger Surround)|
|6 |MPEG 5.1 D (Center, Vänster, Höger, Vänster Surround, Höger Surround, Lågfrekvenseffekter)|
|7 |Apple AAC 6.1 (Center, Vänster, Höger, Vänster Surround, Höger Surround, Center Surround, Lågfrekvenseffekter)|
|8 |MPEG 7.1 B (Center, Vänster Center, Höger Center, Vänster, Höger, Vänster Surround, Höger Surround, Lågfrekvenseffekter)|

## Referenser

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac på GitHub](https://github.com/macosforge/alac)

