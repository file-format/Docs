---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltjene om ALAC filformat og API'er, der kan oprette og åbne ALAC fils.
title: ALAC - Apple Lossless Audio Codec File Format
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Hvad er en ALAC fil?

ALAC-filformatet er Apple Lossless Audio Codec (ALAC), der bruger den MPEG-4-kompatible QuickTime-beholder. Det blev introduceret i 2004 som proprietært filformat, indtil 2011, hvor Apple gjorde det tilgængeligt open source og royaltyfrit. Formatet ligner [FLAC](/audio/flac/) (Free Lossless Audio Codec), men tilbyder mere komprimering sammenligneligt. Det giver et bedre lydende alternativ til [AAC](/audio/aac/) eller [MP3](/audio/mp3/). Lydfiler kodet med ALAC-codec kan åbnes ved hjælp af Apple QuickTime, Apple iTunes og Micrsoft Windows Media Player med K-Lite-codec.

## ALAC filformat

Filer baseret på ALAC codec er binære filer, der er tilgængelige som [open source on GitHub](https://github.com/macosforge/alac) til udviklerens reference. Den indeholder kilderne til ALAC-koderen og dekoderen. Apple har også leveret et kommandolinjeværktøj, kaldet `alacconvert`, til at læse og skrive lyddata til/fra Core Audio Format (CAF) og [WAVE](/audio/wav/) filer. Følgende er nogle nøglepunkter om ALAC-filformatet.

 1. Bitdybder - 16, 20, 24 og 32 bit.
 1. `Sample Rate` - Enhver vilkårlig heltal sample rate fra 1 til 384.000 Hz. Teoretiske hastigheder på op til 4.294.967.295 (2^32 - 1) Hz kunne understøttes.
 1. `Pakkestørrelse` - Standardpakkestørrelsen er som standard 4096 sampleframes af lyd pr. pakke. Andre pakkestørrelser er bestemt mulige. Ikke-standardpakkestørrelser er dog ikke garanteret at fungere korrekt på alle hardwareenheder, der understøtter Apple Lossless. Pakker over 16.384 eksempelrammer understøttes ikke.
 1. Understøttede kanaler' - Den understøtter en til otte kanaler. Hver kanal har følgende rækkefølge af information.

|Num Chan| Bestil|
|---|---|
|1 |mono|
|2 |stereo (venstre, højre)|
|3 |MPEG 3.0 B (Center, Venstre, Højre)|
|4 |MPEG 4.0 B (Center, Venstre, Højre, Center Surround)|
|5 |MPEG 5.0 D (Center, Venstre, Højre, Venstre Surround, Højre Surround)|
|6 |MPEG 5.1 D (Center, Venstre, Højre, Venstre Surround, Højre Surround, Lavfrekvente effekter)|
|7 |Apple AAC 6.1 (Center, Venstre, Højre, Venstre Surround, Højre Surround, Center Surround, Lavfrekvente effekter)|
|8 |MPEG 7.1 B (Center, Venstre Center, Højre Center, Venstre, Højre, Venstre Surround, Højre Surround, Lavfrekvente effekter)|

## Referencer

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)

* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)

* [macosforge - alac på GitHub](https://github.com/macosforge/alac)


