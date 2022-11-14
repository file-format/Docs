---
date: 2022-01-06
keywords: vtt, .vtt, vtt-bestandsformaat, .vtt-bestandsformaat, .vtt-extensie, vtt-extensie
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Meer informatie over .vtt-bestanden en API's die VTT-bestanden kunnen maken en openen."
title: VTT-bestandsindeling - Bestand met webvideoteksttracks
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Wat is een VTT-bestand?

Een VTT-bestand is een tekstbestand dat informatie bevat voor het weergeven van getimede teksttracks (zoals ondertitels of bijschriften) met behulp van de indeling Web Video Text Tracks (WebVTT). De getimede teksttracks bevatten informatie zoals ondertitels of bijschriften. Het doel van het VTT-bestand is om tekstoverlays toe te voegen aan a<video> . Het formaat is enigszins vergelijkbaar met de SRT-bestanden. Op WebVTT gebaseerde tekstbestanden worden gecodeerd met UTF-8. Een VTT-bestand bevat informatie zoals ondertitels, beschrijvingen, bijschriften, beschrijvingen, hoofdstukken en metadata. Omdat het platte tekstbestanden zijn, kunnen VTT-bestanden worden geopend met teksteditors zoals Microsoft Notepad, Apple TextEdit en Notepad++.

## VTT-bestandsindeling - Meer informatie

VTT-bestanden gebruiken het WebVTT-bestandsformaat voor het opslaan van sequentiële teksttrackinformatie. Elke getimede teksttrack bestaat uit een enkele regel of meerdere regels, ook wel een `cue` genoemd, zoals weergegeven in het volgende voorbeeld.

### VTT-bestandsvoorbeeld

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT-bestandsstructuur

Hieronder volgen de structuurvereisten van een VTT-bestand.

* Een optionele byte-ordermarkering (BOM).
* De string "WEBVTT".
* Een optionele tekstkop rechts van WEBVTT.
* Een lege regel, die gelijk is aan twee opeenvolgende nieuwe regels.
* Nul of meer signalen of opmerkingen.
* Nul of meer lege regels.

## Referenties

* [VTT - W3-scholen](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

