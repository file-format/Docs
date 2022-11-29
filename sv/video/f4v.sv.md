---
date: 2019-10-11
keywords: f4v, .f4v, f4v-filformat, .f4v-filformat, .f4v-tillägg, f4v-tillägg, f4v-videoformat, hur man öppnar f4v-filer, vad är f4v-filer
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om F4V-filformat och API:er som kan skapa och öppna F4V-filer" 
title: F4V filformat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Vad är en F4V fil? ##

F4V (Flash MP4 Video File) är en videofil som sparas med filtillägget .f4v. Den är baserad på ISO-basmediafilformatet (MPEG-4 del 12). Den är väldigt lik [MP4](/sv/video/mp4/) varför den också informellt kallas Flash MP4. [FLV](/sv/video/flv/) hade begränsningar vid streaming av H.264/ACC-innehåll vilket resulterade i att Adobe Systems skapade det nya F4V-formatet. Flash Player kan spela F4V-filer sedan släppet av Flash Player 9 Update 3.

## Struktur för F4V-filer ##

F4V-filformatet är baserat på ISO-basmediafilformatet (MPEG-4 del 12) och är mycket likt MP4-formatet. För detaljer om strukturen, se sidan [MP4](/sv/video/mp4/). Den stora skillnaden mellan F4V och MP4 är de metadataformat som F4V kan lagra. Nedan finns en lista över de metadataformat som stöds av F4V-formatet.

- **Taggbox**: Ytterligare fyra valfria taggboxar (auth, title, dscp, cprt) i filmrutan (moov).
- **XMP-metadataruta**: Denna ruta kommer direkt efter filmrutan (moov). Med detta kan filen kommunicera XMP-metadata till en SWF-film genom ActionScript.
- **ilst box**: Denna ruta förekommer i Meta (meta) boxen och kan innehålla ett antal metadatataggar. De datatyper som stöds anges nedan.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Metadataruta för textspår**: Textexemplen (text eller tx3g) inuti Media Databox (mdat). Den kan innehålla följande metadatarutor.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referenser ##

- [Flash-video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

