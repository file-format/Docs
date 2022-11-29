---
date: 2020-08-12
keywords: bpg, .bpg, bpg-filformat, hur man öppnar bpg-filer, .bpg-tillägg, bpg-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG filformat
linktitle: BPG
description: "Lär dig om BPG-filformat och API:er som kan skapa och öppna BPG-filer." 
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Vad är en BPG fil? ##

BPG (Better Portable Graphics) är ett filformat skapat av Fabrice Bellard 2014 för digitala bilder. Han föreslog BPG som en ersättning för JPEG eftersom BPG var mer komprimerings- eller storlekseffektiv. BPG använder intra-frame-kodning av videokomprimeringsstandarden HEVC (High-Efficiency Video Coding).

BPG är designat som ett bärbart minneseffektivt format för att fungera på handhållna enheter och IoT-enheter. För närvarande stöder inte webbläsare BPG-format, men webbplatser kan fortfarande leverera BPG-bilder genom att använda ett JavaScript-bibliotek skrivet av Bellard. BPG använder HEVC:s Main 4:4:4 16 stillbildsprofil upp till 14 bitar per sampel.

## Specifikationer ##

BPG-behållarformatet är ett generiskt bildformat snarare än den råa bitström som används i HEVC. BPG stöder färgformaten 4:4:4, 4:2:2 och 4:2:0. Alfakanalen stöds också med en separat kodad extrakanal eller den fjärde kanalen i CMYK-bilden. BPG tillhandahåller metadatastöd för Exif, ICC-profiler och XMP. BPG stöder YCbCr (ITU-R BT.601, BT.709 och BT.2020 (icke-konstant luminans)), YCgCo, RGB, CMYK och gråskalefärgrymd. BGP stöder också animering och förlustfri och förlustfri HEVC-datakomprimering.

## Referenser ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

