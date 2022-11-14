---
date: 2021-03-21
keywords: alac, alac bestandsformaat, .alac extensie
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lees meer over de ALAC-bestandsindeling en API's die ALAC-bestanden kunnen maken en openen."
title: ALAC - Apple Lossless Audio Codec-bestandsindeling
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Wat is een ALAC-bestand?

De ALAC-bestandsindeling is Apple Lossless Audio Codec (ALAC) die de MPEG-4-compatibele QuickTime-container gebruikt. Het werd in 2004 geïntroduceerd als een eigen bestandsformaat, tot 2011 toen Apple het open source en royaltyvrij beschikbaar maakte. Het formaat is vergelijkbaar met de [FLAC](/nl/audio/flac/) (Free Lossless Audio Codec), maar biedt relatief meer compressie. Het biedt een beter klinkend alternatief voor [AAC](/nl/audio/aac/) of [MP3](/nl/audio/mp3/). Audiobestanden die zijn gecodeerd met ALAC-codec kunnen worden geopend met Apple QuickTime, Apple iTunes en Micrsoft Windows Media Player met K-Lite-codec.

## ALAC-bestandsindeling

Bestanden op basis van de ALAC-codec zijn binaire bestanden die beschikbaar zijn als [open source op GitHub](https://github.com/macosforge/alac) ter referentie van de ontwikkelaar. Het bevat de bronnen voor de ALAC-encoder en -decoder. Apple heeft ook een opdrachtregelhulpprogramma geleverd, genaamd `alacconvert`, om de audiogegevens te lezen en te schrijven naar/van Core Audio Format (CAF) en [WAVE](/nl/audio/wav/)-bestanden. Hieronder volgen enkele belangrijke punten over het ALAC-bestandsformaat.

1. 'Bitdiepten' - 16, 20, 24 en 32 bits.
1. 'Sample Rate' - Elke willekeurige integer sample rate van 1 tot 384.000 Hz. Theoretische snelheden tot 4.294.967.295 (2^32 - 1) Hz kunnen worden ondersteund.
1. `Packet Size` - De standaard pakketgrootte is standaard 4096 sampleframes van audio per pakket. Andere pakketgroottes zijn zeker mogelijk. Het is echter niet gegarandeerd dat niet-standaard pakketgroottes correct werken op alle hardwareapparaten die Apple Lossless ondersteunen. Pakketten boven 16.384 voorbeeldframes worden niet ondersteund.
1. `Ondersteunde kanalen` - Het ondersteunt één tot acht kanalen. Elk kanaal heeft de volgende volgorde van informatie.

|Num Chan| Bestellen|
|---|---|
|1 |mono|
|2 |stereo (links, rechts)|
|3 |MPEG 3.0 B (midden, links, rechts)|
|4 |MPEG 4.0 B (midden, links, rechts, midden surround)|
|5 |MPEG 5.0 D (midden, links, rechts, links surround, rechts surround)|
|6 |MPEG 5.1 D (midden, links, rechts, links surround, rechts surround, lage frequentie-effecten)|
|7 |Apple AAC 6.1 (midden, links, rechts, links surround, rechts surround, midden surround, lage frequentie-effecten)|
|8 |MPEG 7.1 B (midden, links midden, rechts midden, links, rechts, links surround, rechts surround, lage frequentie-effecten)|

## Referenties

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac op GitHub](https://github.com/macosforge/alac)

