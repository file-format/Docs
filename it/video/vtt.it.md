---
date: 2022-01-06
keywords: vtt, .vtt, formato file vtt, formato file .vtt, estensione .vtt, estensione vtt
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Ulteriori informazioni sul file .vtt e sulle API che possono creare e aprire file VTT."
title: Formato file VTT - File di tracce di testo video Web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Che cos'è un file VTT?

Un file VTT è un file di testo che contiene informazioni per la visualizzazione di tracce di testo temporizzate (come sottotitoli o didascalie) utilizzando il formato Web Video Text Tracks (WebVTT). Le tracce di testo a tempo includono informazioni come sottotitoli o didascalie. Lo scopo del file VTT è aggiungere sovrapposizioni di testo a<video> . Il formato è in qualche modo simile ai file SRT. I file di testo basati su WebVTT sono codificati utilizzando UTF-8. Un file VTT contiene informazioni come sottotitoli, descrizioni, didascalie, descrizioni, capitoli e metadati. Essendo file di testo normale, i file VTT possono essere aperti utilizzando editor di testo come Microsoft Notepad, Apple TextEdit e Notepad++.

## Formato file VTT - Ulteriori informazioni

I file VTT utilizzano il formato di file WebVTT per salvare le informazioni sulle tracce di testo sequenziali. Ciascuna traccia di testo a tempo è composta da una o più righe, note anche come "cue", come mostrato nell'esempio seguente.

### Esempio di file VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Struttura del file VTT

Di seguito sono riportati i requisiti di struttura di un file VTT.

* Un byte order mark (BOM) opzionale.
* La stringa "WEBVTT".
* Un'intestazione di testo opzionale a destra di WEBVTT.
* Una riga vuota, che equivale a due nuove righe consecutive.
* Zero o più segnali o commenti.
* Zero o più righe vuote.

## Riferimenti

* [VTT - Scuole W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

