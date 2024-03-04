---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Luždirbti apie ALAC failo formatą ir API, kurios gali sukurti ir atidaryti ALAC failąs.
title: ALAC – „Apple Lossless Audio Codec“ failo formaat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Kas yra ALAC failas?

ALAC failo formatas yra Apple Lossless Audio Codec (ALAC), kuris naudoja su MPEG-4 suderinamą QuickTime konteinerį. Jis buvo pristatytas 2004 m. kaip patentuotas failo formatas iki 2011 m., kai Apple padarė jį prieinamą atviro kodo ir nemokamai. Formatas yra panašus į [FLAC](/audio/flac/) (nemokamą be nuostolių garso kodeką), tačiau siūlo palyginti didesnį glaudinimą. Tai geriau skambanti alternatyva [AAC](/audio/aac/) arba [MP3](/audio/mp3/). Garso failus, užkoduotus ALAC kodeku, galima atidaryti naudojant Apple QuickTime, Apple iTunes ir Micrsoft Windows Media Player su K-Lite kodeku.

## ALAC failo formatas

Failai, pagrįsti ALAC kodeku, yra dvejetainiai failai, kurie kūrėjams pateikiami kaip [open source on GitHub](https://github.com/macosforge/alac). Jame yra ALAC kodavimo ir dekoderio šaltiniai. Apple taip pat pateikė komandų eilutės priemonę, vadinamą alacconvert, skirtą garso duomenims skaityti ir rašyti į pagrindinio garso formato (CAF) ir [WAVE](/audio/wav/) failus arba iš jų. Toliau pateikiami keli pagrindiniai dalykai apie ALAC failo formatą.

 1. Bit Depths - 16, 20, 24 ir 32 bitai.
 1. Sample Rate – bet koks savavališkas sveikųjų skaičių atrankos dažnis nuo 1 iki 384 000 Hz. Galima palaikyti teorinius dažnius iki 4 294 967 295 (2^32 - 1) Hz.
 1. Paketo dydis – numatytasis paketo dydis yra 4096 pavyzdiniai garso kadrai viename pakete. Žinoma, galimi ir kiti paketų dydžiai. Tačiau negarantuojama, kad nenumatytieji paketų dydžiai tinkamai veiks visuose aparatūros įrenginiuose, palaikančiuose Apple Lossless. Paketai, didesni nei 16 384 pavyzdinių kadrų, nepalaikomi.
 1. Palaikomi kanalai – palaiko nuo vieno iki aštuonių kanalų. Kiekviename kanale pateikiama tokia informacijos tvarka.

|Num Chan| Užsakyti|
|---|---|
|1 |mono|
|2 |stereo (kairėn, dešinėn)|
|3 |MPEG 3.0 B (centras, kairė, dešinė)|
|4 |MPEG 4.0 B (centrinis, kairysis, dešinysis, vidurinis erdvinis)|
|5 |MPEG 5.0 D (centrinis, kairysis, dešinysis, kairysis erdvinis, dešinysis erdvinis)|
|6 |MPEG 5.1 D (centrinis, kairysis, dešinysis, kairysis erdvinis, dešinysis erdvinis, žemo dažnio efektai)|
|7 |Apple AAC 6.1 (centrinis, kairysis, dešinysis, kairysis erdvinis, dešinysis erdvinis, centrinis erdvinis, žemo dažnio efektai)|
|8 |MPEG 7.1 B (centras, kairysis centras, dešinysis centras, kairysis, dešinysis, kairysis erdvinis, dešinysis erdvinis, žemo dažnio efektai)|

## Nuorodos

* [ALAC – Vikipedija](https://en.wikipedia.org/wiki/Apple_Lossless)

* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)

* [macosforge – alac „GitHub“](https://github.com/macosforge/alac)


