---
date: 2022-01-06
keywords: vtt, .vtt, vtt fájlformátum, .vtt fájlformátum, .vtt kiterjesztéssel, vtt kiterjesztéssel
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "További információ a .vtt fájlokról és az API-król, amelyek VTT-fájlokat hozhatnak létre és nyithatnak meg."
title: VTT fájlformátum - Web Video szövegsávok fájl
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Mi az a VTT fájl?

A VTT-fájl olyan szöveges fájl, amely információkat tartalmaz az időzített szövegsávok (például feliratok) megjelenítéséhez a Web Video Text Tracks (WebVTT) formátumban. Az időzített szövegsávok olyan információkat tartalmaznak, mint a feliratok. A VTT fájl célja szöveges átfedések hozzáadása a<video> . A formátum némileg hasonlít az SRT fájlokhoz. A WebVTT alapú szöveges fájlok UTF-8 kódolásúak. A VTT-fájl olyan információkat tartalmaz, mint a feliratok, leírások, feliratok, leírások, fejezetek és metaadatok. Mivel egyszerű szöveges fájlok, a VTT fájlok olyan szövegszerkesztőkkel nyithatók meg, mint a Microsoft Notepad, az Apple TextEdit és a Notepad++.

## VTT fájlformátum - További információ

A VTT-fájlok a WebVTT fájlformátumot használják a szekvenciális szövegsávok információinak mentésére. Minden időzített szövegsáv egyetlen sorból vagy több sorból áll, amelyeket „jelnek” is neveznek, amint az a következő példában látható.

### VTT fájl példa

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT fájlszerkezet

Az alábbiakban a VTT-fájl szerkezeti követelményeit mutatjuk be.

* Egy opcionális byte order mark (BOM).
* A "WEBVTT" karakterlánc.
* Egy opcionális szövegfejléc a WEBVTT jobb oldalán.
* Üres sor, amely két egymást követő újsornak felel meg.
* Nulla vagy több jelzés vagy megjegyzés.
* Nulla vagy több üres sor.

## Hivatkozások

* [VTT – W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT – Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

