---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LVTT faylı yarada və aça bilən .vtt faylı və API-lər haqqında qazanıns.
title: VTT Fayl Format - Web Video Mətn Tracks File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-azt"
    parent: "video"
lastmod: 2022-01-06
---

## VTT faylı nədir?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT Fayl Format - Ətraflı məlumat

VTT faylları ardıcıl mətn izləri məlumatını saxlamaq üçün WebVTT fayl formatından istifadə edir. Hər bir vaxt təyin edilmiş mətn treki, aşağıdakı misalda göstərildiyi kimi, istək” kimi də tanınan tək sətirdən və ya bir neçə sətirdən ibarətdir.

### VTT fayl nümunəsi

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT Fayl Strukturu

Aşağıda VTT faylının struktur tələbləri verilmişdir.

 * İsteğe bağlı bayt sıra işarəsi (BOM).
 * WEBVTT sətri.
 * WEBVTT-nin sağında isteğe bağlı mətn başlığı.
 * Ardıcıl iki yeni sətirə bərabər olan boş sətir.
 * Sıfır və ya daha çox işarə və ya şərh.
 * Sıfır və ya daha çox boş sətir.

## İstinadlar

 * [VTT - W3 Məktəbləri](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

