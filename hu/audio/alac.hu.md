---
date: 2021-03-21
keywords: alac, alac fájlformátum, .alac kiterjesztése
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Ismerje meg az ALAC fájlformátumot és az API-kat, amelyek ALAC fájlokat hozhatnak létre és nyithatnak meg."
title: ALAC - Apple Lossless Audio Codec fájlformátum
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Mi az ALAC fájl?

Az ALAC fájlformátum egy Apple Lossless Audio Codec (ALAC), amely az MPEG-4 kompatibilis QuickTime tárolót használja. 2004-ben vezették be védett fájlformátumként, egészen 2011-ig, amikor az Apple nyílt forráskódú és jogdíjmentesen elérhetővé tette. A formátum hasonló a [FLAC](/hu/audio/flac/)-hez (ingyenes veszteségmentes audiokodek), de ehhez képest több tömörítést kínál. Jobb hangzású alternatívát kínál az [AAC](/hu/audio/aac/) vagy az [MP3](/hu/audio/mp3/) helyett. Az ALAC kodekkel kódolt hangfájlok Apple QuickTime, Apple iTunes és Micrsoft Windows Media Player K-Lite kodekkel nyithatók meg.

## ALAC fájlformátum

Az ALAC kodeken alapuló fájlok bináris fájlok, amelyek [nyílt forráskódként a GitHubon](https://github.com/macosforge/alac) érhetők el fejlesztői hivatkozásként. Tartalmazza az ALAC kódoló és dekódoló forrásait. Az Apple egy parancssori segédprogramot is biztosított, az úgynevezett "alacconvert", amely a hangadatokat Core Audio Format (CAF) és [WAVE](/hu/audio/wav/) fájlba/azokból írhatja. Az alábbiakban néhány kulcsfontosságú pontot olvashat az ALAC fájlformátumról.

1. "Bitmélység" - 16, 20, 24 és 32 bit.
1. "Mintavételi frekvencia" – tetszőleges egész számú mintavételi frekvencia 1 és 384 000 Hz között. Akár 4 294 967 295 (2^32 - 1) Hz elméleti sebesség is támogatható.
1. "Csomagméret" - Az alapértelmezett csomagméret alapértelmezés szerint 4096 hangminta keret csomagonként. Természetesen más csomagméretek is lehetségesek. A nem alapértelmezett csomagméretek azonban nem garantáltan megfelelően fognak működni minden olyan hardvereszközön, amely támogatja az Apple Lossless-t. A 16 384 mintakockát meghaladó csomagok nem támogatottak.
1. "Támogatott csatornák" - 1-8 csatornát támogat. Minden csatornán a következő információk állnak rendelkezésre.

|Num Chan| Rendelés|
|---|---|
|1 |mono|
|2 |sztereó (bal, jobb)|
|3 |MPEG 3.0 B (középen, balra, jobbra)|
|4 |MPEG 4.0 B (középen, balra, jobbra, középső térhangzás)|
|5 |MPEG 5.0 D (középső, bal, jobb, bal oldali térhangzás, jobb oldali térhangzás)|
|6 |MPEG 5.1 D (középső, bal, jobb, bal oldali térhangzás, jobb oldali térhangzás, alacsony frekvenciájú effektusok)|
|7 |Apple AAC 6.1 (középső, bal, jobb, bal oldali térhangzás, jobb oldali térhangzás, középső térhangzás, alacsony frekvenciájú effektusok)|
|8 |MPEG 7.1 B (közép, bal közép, jobb középső, bal, jobb, bal oldali térhangzás, jobb térhatás, alacsony frekvenciájú effektusok)|

## Hivatkozások

* [ALAC – Wikipédia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac a GitHubon](https://github.com/macosforge/alac)

