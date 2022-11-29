---
date: 2022-01-06
keywords: vtt, .vtt, vtt-filformat, .vtt-filformat, .vtt-tillägg, vtt-tillägg
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig mer om .vtt-filer och API:er som kan skapa och öppna VTT-filer." 
title: VTT-filformat - Webbvideotextspårfil
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Vad är VTT fil?

En VTT-fil är en textfil som innehåller information för att visa tidsinställda textspår (som undertexter) med hjälp av Web Video Text Tracks (WebVTT)-format. De tidsinställda textspåren innehåller information som undertexter eller bildtexter. Syftet med VTT-filen är att lägga till textöverlägg till en<video> . Formatet är lite likt SRT-filerna. WebVTT-baserade textfiler kodas med UTF-8. En VTT-fil innehåller information såsom undertexter, beskrivningar, bildtexter, beskrivningar, kapitel och metadata. Eftersom de är vanliga textfiler kan VTT-filer öppnas med textredigerare som Microsoft Notepad, Apple TextEdit och Notepad++.

## VTT-filformat - Mer information

VTT-filer använder filformatet WebVTT för att spara information om sekventiell textspår. Varje tidsbestämt textspår består av en enda rad eller flera rader, även känd som en "cue" som visas i följande exempel.

### VTT-filexempel

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT-filstruktur

Följande är strukturkraven för en VTT-fil.

* En valfri byte ordermark (BOM).
* Strängen "WEBVTT".
* En valfri textrubrik till höger om WEBVTT.
* En tom rad, vilket motsvarar två på varandra följande nyrader.
* Noll eller fler ledtrådar eller kommentarer.
* Noll eller fler tomma rader.

## Referenser

* [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

