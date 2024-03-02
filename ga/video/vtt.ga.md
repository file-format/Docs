---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lthuilleamh faoi chomhad .vtt agus APIs ar féidir leo comhad VTT a chruthú agus a oscailts.
title: VFormáid Chomhaid TT - Rianta Téacs Físeáin Gréasáin File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-gat"
    parent: "video"
lastmod: 2022-01-06
---

## Cad is comhad VTT ann?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## Formáid Chomhaid VTT - Tuilleadh eolais

Úsáideann comhaid VTT formáid comhaid WebVTT chun faisnéis rianta téacs seicheamhach a shábháil. Is éard atá i ngach rian téacs amaithe ná líne shingil nó línte iolracha, ar a dtugtar `cue` freisin mar a thaispeántar sa sampla seo a leanas.

### Sampla Comhad VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Struchtúr Comhad VTT

Seo a leanas na riachtanais struchtúir a bhaineann le comhad VTT.

 * Marc ordaithe beart roghnach (BOM).
 * An teaghrán WEBVTT.
 * Ceanntásc téacs roghnach ar thaobh na láimhe deise de WEBVTT.
 * Líne bhán, atá comhionann le dhá líne nua as a chéile.
 * Leideanna nó tuairimí nialais nó níos mó.
 * Línte bán nialais nó níos mó.

## Tagairtí

 * [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

