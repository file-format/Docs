---
date: 2021-03-21
keywords: alac, format de fișier alac, extensia .alac
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Aflați despre formatul de fișier ALAC și despre API-urile care pot crea și deschide fișiere ALAC."
title: ALAC - Format de fișier Apple Lossless Audio Codec
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Ce este un fișier ALAC?

Formatul de fișier ALAC este Apple Lossless Audio Codec (ALAC) care utilizează containerul QuickTime compatibil MPEG-4. A fost introdus în 2004 ca format de fișier proprietar, până în 2011, când Apple l-a făcut disponibil open source și fără drepturi de autor. Formatul este similar cu [FLAC](/ro/audio/flac/) (Codec audio gratuit fără pierderi), dar oferă mai multă compresie comparativ. Oferă o alternativă de sunet mai bună la [AAC](/ro/audio/aac/) sau [MP3](/ro/audio/mp3/). Fișierele audio codificate cu codecul ALAC pot fi deschise utilizând Apple QuickTime, Apple iTunes și Microsoft Windows Media Player cu codecul K-Lite.

## Format de fișier ALAC

Fișierele bazate pe codecul ALAC sunt fișiere binare care sunt disponibile ca [sursă deschisă pe GitHub](https://github.com/macosforge/alac) pentru referința dezvoltatorului. Conține sursele pentru codificatorul și decodorul ALAC. Apple a furnizat, de asemenea, un utilitar de linie de comandă, numit `alaconvert`, pentru a citi și scrie datele audio în/din fișierele Core Audio Format (CAF) și [WAVE](/ro/audio/wav/). Următoarele sunt câteva puncte cheie despre formatul de fișier ALAC.

1. „Adancime de biți” - 16, 20, 24 și 32 de biți.
1. „Rata de eșantionare” - Orice frecvență de eșantionare între 1 și 384.000 Hz. Pot fi acceptate rate teoretice de până la 4.294.967.295 (2^32 - 1) Hz.
1. `Dimensiunea pachetului` - Dimensiunea implicită a pachetului este implicită la 4096 de cadre de probă audio per pachet. Alte dimensiuni de pachete sunt cu siguranță posibile. Cu toate acestea, dimensiunile de pachete care nu sunt implicite nu sunt garantate să funcționeze corect pe toate dispozitivele hardware care acceptă Apple Lossless. Pachetele de peste 16.384 de cadre de probă nu sunt acceptate.
1. `Canale acceptate` - Acceptă unul până la opt canale. Fiecare canal are următoarea ordine de informații.

|Număr Chan| Comanda|
|---|---|
|1 |mono|
|2 |stereo (stânga, dreapta)|
|3 |MPEG 3.0 B (Centru, Stânga, Dreapta)|
|4 |MPEG 4.0 B (Centru, Stânga, Dreapta, Centru Surround)|
|5 |MPEG 5.0 D (Centru, Stânga, Dreapta, Stânga Surround, Dreapta Surround)|
|6 |MPEG 5.1 D (Centru, Stânga, Dreapta, Stânga Surround, Dreapta Surround, Efecte de joasă frecvență)|
|7 |Apple AAC 6.1 (Centru, Stânga, Dreapta, Stânga Surround, Dreapta Surround, Centru Surround, Efecte de joasă frecvență)|
|8 |MPEG 7.1 B (Centru, Stânga Centru, Dreapta Centru, Stânga, Dreapta, Stânga Surround, Dreapta Surround, Efecte de joasă frecvență)|

## Referințe

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Codec audio Apple Lossless](https://macosforge.github.io/alac/)
* [macosforge - alac pe GitHub](https://github.com/macosforge/alac)

