---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om F4V filformat og API'er, der kan oprette og åbne F4V files
title: F4V fil formularat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Hvad er en F4V fil? ##

F4V (Flash MP4 Video File) er en videofil, der er gemt med filtypenavnet .f4v. Det er baseret på ISO-basemediefilformatet (MPEG-4 del 12). Den minder meget om [MP4](/video/mp4/), hvorfor den også uformelt omtales som Flash MP4. [FLV](/video/flv/) havde begrænsninger ved streaming af H.264/ACC-indhold, hvilket resulterede i, at Adobe Systems oprettede det nye F4V-format. Flash Player kan afspille F4V-filer siden udgivelsen af Flash Player 9 Update 3.

## Struktur af F4V-filer ##

F4V-filformatet er baseret på ISO-basemediefilformatet (MPEG-4 Part 12) og minder meget om MP4-formatet. For detaljer om strukturen, se venligst [MP4](/video/mp4/)-siden. Den største forskel mellem F4V og MP4 er de metadataformater, som F4V kan gemme. Nedenfor er listen over de metadataformater, der understøttes af F4V-formatet.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP Metadata boks**: Denne boks kommer lige efter Movie (moov) boksen. Med dette kan filen kommunikere XMP-metadata til en SWF-film gennem ActionScript.
- **Ilst box**: Denne boks findes inde i Meta (meta) boksen og kan indeholde en række metadata tags. De understøttede datatyper er angivet nedenfor.
  - "**0**: Tilpassede data."
  - "**1**: Tekstdata."
  - "**12, 14**: Binære data"
  - "**21**: Generiske data."
- **Tekstspormetadatafelt**: Teksteksemplerne (tekst eller tx3g) inde i mediedataboksen (mdat). Den kan indeholde følgende metadatabokse.
  - "**Stilboks**: Specifikationer for tekststil."
  - "**Fremhæv boks**: Specificerer rækkevidden af tekst, der skal fremhæves."
  - "**Højlysfarvefelt**: Specificerer tekstens fremhævelsesfarve."
  - "**Karaoke-boks**: Angiv karaoke-metadata."
  - "**Rulningsforsinkelse boks**: Specificerer rulleforsinkelsen."
  - "**Drop Shadow Offset box**: Specificerer drop shadow offset-koordinaterne for teksten."
  - "**Drop Shadow Alpha box**: Specificerer drop shadow alpha værdien for teksten."
  - "**Hypertekstboks**: Specificerer hypertekstteksten med alternativ tekst over et tekstområde."
  - "**Tekstboksboks**: Definerer koordinaterne for tekstboksen."
  - "**Blinkende boks**: Specificerer blink for en række tekst."
  - "**Tekstombrydningsfelt**: Indstiller tekstombrydningsflaget for teksten."
  - "**Tekstombrydningsfelt**: Indstiller tekstombrydningsflaget for teksten."

## Referencer ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

