---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lnopelniet par ALAC faila formātu un API, kas var izveidot un atvērt ALAC failus.
title: ALAC — Apple bezzudumu audio kodeka faila veidlapaat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Kas ir ALAC fails?

ALAC faila formāts ir Apple Lossless Audio Codec (ALAC), kas izmanto MPEG-4 saderīgu QuickTime konteineru. Tas tika ieviests 2004. gadā kā patentēts faila formāts, līdz 2011. gadā Apple padarīja to pieejamu atvērtā koda formātā un bez autoratlīdzības. Formāts ir līdzīgs [FLAC](/audio/flac/) (Free Lossless Audio Codec), taču piedāvā salīdzinoši lielāku saspiešanu. Tas piedāvā labāk skanošu alternatīvu [AAC](/audio/aac/) vai [MP3](/audio/mp3/). Audio failus, kas kodēti ar ALAC kodeku, var atvērt, izmantojot Apple QuickTime, Apple iTunes un Micrsoft Windows Media Player ar K-Lite kodeku.

## ALAC faila formāts

Faili, kuru pamatā ir ALAC kodeku, ir bināri faili, kas izstrādātāja atsaucei ir pieejami kā [open source on GitHub](https://github.com/macosforge/alac). Tajā ir ALAC kodētāja un dekodētāja avoti. Apple ir arī nodrošinājis komandrindas utilītu, ko sauc par alacconvert, lai nolasītu un ierakstītu audio datus uz/no Core Audio Format (CAF) un [WAVE](/audio/wav/) failiem. Tālāk ir minēti daži galvenie punkti par ALAC faila formātu.

 1. Bitu dziļums - 16, 20, 24 un 32 biti.
 1. Iztveršanas ātrums — jebkura patvaļīga vesela skaitļa izlases frekvence no 1 līdz 384 000 Hz. Var atbalstīt teorētiskos ātrumus līdz 4 294 967 295 (2^32 - 1) Hz.
 1. Pakešu lielums — noklusējuma pakešu lielums ir 4096 audio paraugkadri katrā paketē. Noteikti ir iespējami arī citi paciņu izmēri. Tomēr netiek garantēts, ka pakešu izmēri, kas nav noklusējuma izmēri, pareizi darbosies visās aparatūras ierīcēs, kas atbalsta Apple Lossless. Paketes, kas pārsniedz 16 384 paraugu kadrus, netiek atbalstītas.
 1. Atbalstītie kanāli — atbalsta no viena līdz astoņiem kanāliem. Katram kanālam ir šāda informācijas secība.

|Num Chan| Pasūtīt|
|---|---|
|1 |mono|
|2 |stereo (pa kreisi, pa labi)|
|3 |MPEG 3.0 B (centrā, pa kreisi, pa labi)|
|4 |MPEG 4.0 B (centrā, pa kreisi, pa labi, centrālais telpiskais)|
|5 |MPEG 5.0 D (centrā, pa kreisi, pa labi, pa kreisi ieskauj, pa labi)|
|6 |MPEG 5.1 D (centrā, pa kreisi, pa labi, pa kreisi telpiskā skaņa, labā telpiskā skaņa, zemas frekvences efekti)|
|7 |Apple AAC 6.1 (centra, kreisā, labā, kreisā telpiskā, labā telpiskā, centra telpiskā skaņa, zemas frekvences efekti)|
|8 |MPEG 7.1 B (centrs, kreisais centrs, pa labi centrs, pa kreisi, pa labi, pa kreisi telpiskā skaņa, labā telpiskā skaņa, zemas frekvences efekti)|

## Atsauces

* [ALAC — Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)

* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)

* [macosforge — alac vietnē GitHub](https://github.com/macosforge/alac)


