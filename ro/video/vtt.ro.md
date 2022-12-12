---
date: 2022-01-06
keywords: vtt, .vtt, format de fișier vtt, format de fișier .vtt, extensie .vtt, extensie vtt
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Aflați despre fișierul .vtt și API-urile care pot crea și deschide fișiere VTT."
title: Format de fișier VTT - Fișier Web Video Text Tracks
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Ce este un fișier VTT?

Un fișier VTT este un fișier text care conține informații pentru afișarea melodiilor de text cronometrate (cum ar fi subtitrări sau subtitrări) folosind formatul Web Video Text Tracks (WebVTT). Piesele de text cronometrate includ informații precum subtitrări sau subtitrări. Scopul fișierului VTT este de a adăuga suprapuneri de text la un<video> . Formatul este oarecum similar cu fișierele SRT. Fișierele text bazate pe WebVTT sunt codificate folosind UTF-8. Un fișier VTT conține informații precum subtitrări, descrieri, subtitrări, descrieri, capitole și metadate. Fiind fișiere text simplu, fișierele VTT pot fi deschise folosind editori de text precum Microsoft Notepad, Apple TextEdit și Notepad++.

## Format de fișier VTT - Mai multe informații

Fișierele VTT utilizează formatul de fișier WebVTT pentru salvarea informațiilor secvențiale ale pieselor text. Fiecare pistă de text cronometrată constă dintr-o singură linie sau mai multe linii, cunoscută și sub numele de „tac”, așa cum se arată în exemplul următor.

### Exemplu de fișier VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Structura fișierului VTT

Următoarele sunt cerințele de structură ale unui fișier VTT.

* Un marcaj opțional de ordine a octetilor (BOM).
* Șirul „WEBVTT”.
* Un antet text opțional în dreapta WEBVTT.
* O linie goală, care este echivalentă cu două linii noi consecutive.
* Zero sau mai multe indicii sau comentarii.
* Zero sau mai multe linii goale.

## Referințe

* [VTT - Școli W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

