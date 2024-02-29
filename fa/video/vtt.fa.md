---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lدر مورد فایل vtt. و APIهایی که می توانند فایل VTT را ایجاد و باز کنند، کسب کنیدs.
title: Vفرمت فایل TT - آهنگ های متنی ویدئوی وب فیle
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-fat"
    parent: "video"
lastmod: 2022-01-06
---

## فایل VTT چیست؟

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## فرمت فایل VTT - اطلاعات بیشتر

فایل های VTT از فرمت فایل WebVTT برای ذخیره اطلاعات آهنگ های متنی متوالی استفاده می کنند. هر تراک متنی زمان‌بندی‌شده از یک خط یا چند خط تشکیل شده است که همانطور که در مثال زیر نشان داده شده است به عنوان «Cue» نیز شناخته می‌شود.

### مثال فایل VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### ساختار فایل VTT

در زیر الزامات ساختار یک فایل VTT آورده شده است.

 * یک علامت سفارش بایت اختیاری (BOM).
 * رشته WEBVTT.
 * یک سرصفحه متن اختیاری در سمت راست WEBVTT.
 * یک خط خالی که معادل دو خط جدید متوالی است.
 * صفر یا بیشتر نشانه یا نظرات.
 * صفر یا بیشتر خطوط خالی

## منابع

 * [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

