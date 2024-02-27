---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om VOB filformat og API'er, der kan oprette og åbne VOB fils.
title: VOB fil formularat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Hvad er en VOB fil? ##

VOB-filer gemmes typisk i VIDEO_TS-biblioteket på en DVD med filtypenavnet .vob. VOB-filer indeholder video- og lyddata samt andre data som menuer og undertekster. VOB er baseret på MPEG-2 program stream format, men det har yderligere begrænsninger og specifikationer i private streams. VOB-filer er en streng undergruppe af MPEG-programstrømme, så alle VOB-filer er MPEG-programstrømme, men alle MPEG-programstrømme er ikke VOB-kompatible.

## Struktur af DVD Video ##

Når en DVD åbnes på en computer, er VIDEO_TS den øverste mappe med AUDIO_TS. AUDIO_TS er tom og bruges ikke. Inde i VIDEO_TS-mappen er der VOB-, BUP- og IFO-filer. VOB-filer indeholder MPEG-indholdet. Disse er opdelt i 1 GB eller mindre bidder, så disse er kompatible med alle operativsystemer. IFO-filerne indeholder information om menuerne og titelstrukturen. BUK-filerne er backup-filer af IFO-filerne med samme navn. Disse filer er beregnet til at blive opbevaret i et separat område fysisk, så i tilfælde af at IFO-filen er beskadiget på grund af fysisk skade på DVD'en, kan BUK-filen give de samme oplysninger.

### Fysisk layout ###

- Alle filer på disken skal være sammenhængende.
- De relaterede filer skal være ved siden af hinanden (VOB, IFO, BUP).
- De nummererede filer skal være i stigende rækkefølge.

## Kopibeskyttelse ##

Mange video-dvd'er er krypteret og forhindrer kopiering af data fra dvd'en. Godkendelses- og dekrypteringsnøgler er nødvendige for at afspille de filer, der er placeret i det utilgængelige indføringsområde på DVD'en. Disse nøgler bruges af CSS-dekrypteringssoftwaren, der findes i DVD-afspilleren eller softwareafspilleren. Uden tasterne kan videofilerne ikke afspilles, da tasterne vil blive anmodet om, når filerne åbnes.

## Referencer ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

