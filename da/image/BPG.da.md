---
date: 2020-08-12
keywords: bpg, .bpg, bpg file format, how to open bpg files, .bpg extension, bpg extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG fil formularat
linktitle: BPG
description: Ltjene om BPG filformat og API'er, der kan oprette og åbne BPG fils.
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Hvad er en BPG fil? ##

BPG (Better Portable Graphics) er et filformat skabt af Fabrice Bellard i 2014 til digitale billeder. Han foreslog BPG som en erstatning for JPEG, da BPG var mere komprimerings- eller størrelseseffektiv. BPG bruger intra-frame-kodning af HEVC (High-Efficiency Video Coding) videokomprimeringsstandard.

BPG er designet som et bærbart hukommelseseffektivt format til at fungere på håndholdte og IoT-enheder. I øjeblikket understøtter webbrowsere ikke BPG-format, men websteder kan stadig levere BPG-billeder ved at bruge et JavaScript-bibliotek skrevet af Bellard. BPG bruger HEVC's Main 4:4:4 16 Still Picture-profil op til 14 bits pr. sample.

## Specifikationer ##

BPG-beholderformatet er et generisk billedformat i stedet for den rå bitstream, der bruges i HEVC. BPG understøtter 4:4:4, 4:2:2 og 4:2:0 farveformater. Alfakanal understøttes også med en separat kodet ekstra kanal eller den fjerde kanal af CMYK-billede. BPG leverer metadataunderstøttelse til Exif, ICC-profiler og XMP. BPG understøtter YCbCr (ITU-R BT.601, BT.709 og BT.2020 (ikke-konstant luminans)), YCgCo, RGB, CMYK og gråtonefarverum. BGP understøtter også animation og tabs- og tabsfri HEVC-datakomprimering.

## Referencer ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

