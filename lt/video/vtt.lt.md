---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Luždirbkite apie .vtt failą ir API, kurios gali sukurti ir atidaryti VTT failąs.
title: VTT failo formatas – žiniatinklio vaizdo įrašo teksto takeliai File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-ltt"
    parent: "video"
lastmod: 2022-01-06
---

## Kas yra VTT failas?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT failo formatas – daugiau informacijos

VTT failai naudoja WebVTT failo formatą nuoseklių teksto takelių informacijai išsaugoti. Kiekvieną teksto takelį pagal laiką sudaro viena eilutė arba kelios eilutės, taip pat žinomos kaip pažyma, kaip parodyta toliau pateiktame pavyzdyje.

### VTT failo pavyzdys

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT failo struktūra

Toliau pateikiami VTT failo struktūros reikalavimai.

 * Neprivalomas baitų eilės ženklas (BOM).
 * Styga WEBVTT.
 * Pasirenkama teksto antraštė dešinėje WEBVTT.
 * Tuščia eilutė, kuri atitinka dvi naujas eilutes iš eilės.
 * Nulis ar daugiau užuominų ar komentarų.
 * Nulis arba daugiau tuščių eilučių.

## Nuorodos

 * [VTT – W3 mokyklos](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

