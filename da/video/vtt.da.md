---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltjen omkring .vtt-fil og API'er, der kan oprette og åbne VTT-fils.
title: VTT-filformat - Webvideotekstspor File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-dat"
    parent: "video"
lastmod: 2022-01-06
---

## Hvad er VTT fil?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT-filformat - Flere oplysninger

VTT-filer bruger WebVTT-filformatet til at gemme sekventielle tekstsporoplysninger. Hvert tidsbestemt tekstspor består af en enkelt linje eller flere linjer, også kendt som en cue som vist i følgende eksempel.

### VTT-fileksempel

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT-filstruktur

Følgende er strukturkravene til en VTT-fil.

 * Et valgfrit byteordremærke (BOM).
 * Strengen WEBVTT.
 * En valgfri tekstoverskrift til højre for WEBVTT.
 * En tom linje, som svarer til to på hinanden følgende nye linjer.
 * Nul eller flere signaler eller kommentarer.
 * Nul eller flere tomme linjer.

## Referencer

 * [VTT - W3 Skoler](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

