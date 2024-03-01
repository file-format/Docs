---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lansaitse noin .vtt-tiedostoa ja API:ita, jotka voivat luoda ja avata VTT-tiedostons.
title: VTT-tiedostomuoto - Web-videotekstiraitoja File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-fit"
    parent: "video"
lastmod: 2022-01-06
---

## Mikä on VTT-tiedosto?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT-tiedostomuoto - Lisätietoja

VTT-tiedostot käyttävät WebVTT-tiedostomuotoa peräkkäisten tekstiraitojen tietojen tallentamiseen. Jokainen ajastettu tekstiraita koostuu yhdestä rivistä tai useista riveistä, joita kutsutaan myös vihjeeksi, kuten seuraavassa esimerkissä näkyy.

### VTT-tiedostoesimerkki

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT:n tiedostorakenne

Seuraavassa on VTT-tiedoston rakennevaatimukset.

 * Valinnainen tavujärjestysmerkki (BOM).
 * Merkkijono WEBVTT.
 * Valinnainen tekstiotsikko WEBVTT:n oikealla puolella.
 * Tyhjä rivi, joka vastaa kahta peräkkäistä rivinvaihtoa.
 * Nolla tai enemmän vihjeitä tai kommentteja.
 * Nolla tai useampia tyhjiä rivejä.

## Viitteet

 * [VTT – W3 Schools](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

