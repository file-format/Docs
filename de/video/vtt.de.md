---
date: 2022-01-06
keywords: "vtt, .vtt, vtt-Dateiformat, .vtt-Dateiformat, .vtt-Erweiterung, vtt-Erweiterung"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Erfahren Sie mehr über .vtt-Dateien und APIs, die VTT-Dateien erstellen und öffnen können."
title: "VTT-Dateiformat - Webvideo-Textspurdatei"
linktitle: "VTT"
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Was ist eine VTT-Datei?

Eine VTT-Datei ist eine Textdatei, die Informationen zum Anzeigen von zeitgesteuerten Textspuren (z. B. Untertitel oder Beschriftungen) im Format Web Video Text Tracks (WebVTT) enthält. Die zeitgesteuerten Textspuren enthalten Informationen wie Untertitel oder Bildunterschriften. Der Zweck der VTT-Datei besteht darin, Textüberlagerungen zu einer hinzuzufügen<video> . Das Format ist den SRT-Dateien etwas ähnlich. WebVTT-basierte Textdateien werden mit UTF-8 kodiert. Eine VTT-Datei enthält Informationen wie Untertitel, Beschreibungen, Beschriftungen, Beschreibungen, Kapitel und Metadaten. Als reine Textdateien können VTT-Dateien mit Texteditoren wie Microsoft Notepad, Apple TextEdit und Notepad++ geöffnet werden.

## VTT-Dateiformat - Weitere Informationen

VTT-Dateien verwenden das WebVTT-Dateiformat zum Speichern von Informationen zu sequentiellen Textspuren. Jede zeitgesteuerte Textspur besteht aus einer einzelnen Zeile oder mehreren Zeilen, die auch als „Cue“ bezeichnet werden, wie im folgenden Beispiel gezeigt.

### VTT-Dateibeispiel

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT-Dateistruktur

Im Folgenden sind die Strukturanforderungen einer VTT-Datei aufgeführt.

* Eine optionale Byte-Order-Marke (BOM).
* Die Zeichenfolge „WEBVTT“.
* Eine optionale Textüberschrift rechts von WEBVTT.
* Eine Leerzeile, die zwei aufeinanderfolgenden Zeilenumbrüchen entspricht.
* Null oder mehr Hinweise oder Kommentare.
* Null oder mehr Leerzeilen.

## Verweise

* [VTT - W3-Schulen] (https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

