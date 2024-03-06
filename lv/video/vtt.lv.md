---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lnopelniet par .vtt failu un API, kas var izveidot un atvērt VTT failus.
title: VTT faila formāts — tīmekļa video teksta ieraksti File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-lvt"
    parent: "video"
lastmod: 2022-01-06
---

## Kas ir VTT fails?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT faila formāts — vairāk informācijas

VTT faili izmanto WebVTT faila formātu, lai saglabātu secīgu teksta celiņu informāciju. Katrs noteiktais teksta celiņš sastāv no vienas rindiņas vai vairākām rindiņām, kas pazīstamas arī kā norāde”, kā parādīts nākamajā piemērā.

### VTT faila piemērs

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT faila struktūra

Tālāk ir norādītas VTT faila struktūras prasības.

 * Izvēles baitu secības zīme (BOM).
 * Virkne WEBVTT.
 * Izvēles teksta galvene pa labi no WEBVTT.
 * Tukša rinda, kas ir līdzvērtīga divām secīgām jaunām rindiņām.
 * Nulle vai vairāk norāžu vai komentāru.
 * Nulle vai vairāk tukšu rindu.

## Atsauces

 * [VTT — W3 skolas](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

