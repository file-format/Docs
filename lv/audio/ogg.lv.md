---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par OGG faila formātu un API, kas var izveidot un atvērt OGG failus.
title: OGG fails — Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Kas ir OGG fails?

OGG ir Ogg Vorbis saspiests audio fails, kas tiek saglabāts ar paplašinājumu .ogg. OGG faili tiek izmantoti audio datu glabāšanai, un tie var ietvert arī izpildītāju un ierakstu informāciju, kā arī metadatus. OGG ir bezmaksas un atvērts konteinera formāts, ko uztur Xiph.Org Foundation.

## Īsa OGG faila formāta vēsture

Ogg projekts sākās kā daļa no lielāka projekta 1993. gadā un tika nosaukts par Squish, taču esošās preču zīmes dēļ tas tika pārdēvēts par OggSquish. Tas tika aprakstīts kā mēģinājums izveidot elastīgu saspiestu audio formātu mūsdienu audio lietojumprogrammām. OGG atsauce tika atdalīta no Vorbis 2000. gada 2. septembrī.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. Līdz 2009. gada 30. jūnijam OGG bija vienīgais konteinera formāts, ko atbalstīja Firefox 3.5 HTML5 ieviešana.

## OGG faila formāts

OGG formāts sastāv no datu daļām. Katru gabalu sauc par Ogg lapu. Katra lapa sākas ar OggS, lai identificētu Ogg formātu. Galvenē ir sērijas numurs un lapas numurs, kas identificē katru lapu kā sērijas daļu. Lapa sastāv no šādām sastāvdaļām.

- **Lapas galvene**
  - "**Capture Pattern (32 bits)**: to izmanto sinhronizācijai, parsējot OGG failus."
  - "**Versija (8 biti)**: norāda Ogg bitu straumes versiju."
  - "**Galvenes veids (8 biti)**: norāda lapas veidu."

| Bits | Vērtība | Apraksts |
| --- | --- | --- |
| 0 | 0x01 | Norāda, ka lapas pirmā pakete ir iepriekšējās paketes turpinājums loģiskajā bitu plūsmā. |
| 1 | 0x02 | Norāda, ka šī lapa ir pirmā loģiskajā bitu plūsmā. |
| 2 | 0x04 | Norāda, ka šī lapa ir pēdējā loģiskajā bitu plūsmā. |

  - "**Granula pozīcija (64 biti)**: tas ir laika marķieris, kura nozīmi nosaka kodeks."
  - "**Bitu straumes sērijas numurs (32 biti)**: tas ir sērijas numurs, kas identificē lapu, kas pieder noteiktai loģiskai bitu straumei."
  - "**Lapas kārtas numurs (32 biti)**: norāda tās lapas secību, kuras pirmā lapa sākas ar 0."
  - "**Kontrolsumma (32 biti)**: nodrošina visu lapas datu CRC32 kontrolsummu."
  - "**Lapas segmenti (8 biti)**: norāda segmentu skaitu lapā."
  - "**Segmentu tabula**: tas ir 8 bitu vērtību masīvs, kas norāda katra segmenta garumu lapas pamattekstā."
- **Metadati**: VorbisComment ir visplašāk atbalstītais metadatu glabāšanas mehānisms. Citi mehānismi ir šādi:
  - "FLAC metadatu bloki"
  - "Oga skelets"
  - "Nepārtraukta multivides iezīmēšanas valoda"

## Atsauces Nr.

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

