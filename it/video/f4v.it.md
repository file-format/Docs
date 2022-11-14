---
date: 2019-10-11
keywords: f4v, .f4v, formato file f4v, formato file .f4v, estensione .f4v, estensione f4v, formato video f4v, come aprire file f4v, cosa sono i file f4v
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file F4V e le API che possono creare e aprire file F4V"
title: Formato file F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Che cos'è un file F4V? ##

F4V (File video Flash MP4) è un file video salvato con estensione .f4v. Si basa sul formato file multimediale di base ISO (MPEG-4 Parte 12). È molto simile a [MP4](/it/video/mp4/), motivo per cui viene anche chiamato in modo informale Flash MP4. [FLV](/it/video/flv/) presentava limitazioni durante lo streaming di contenuti H.264/ACC, il che ha portato Adobe Systems a creare il nuovo formato F4V. Flash Player può riprodurre file F4V dal rilascio di Flash Player 9 Update 3.

## Struttura dei file F4V ##

Il formato file F4V si basa sul formato file multimediale di base ISO (MPEG-4 Parte 12) ed è molto simile al formato MP4. Per i dettagli riguardanti la struttura, vedere la pagina [MP4](/it/video/mp4/). La principale differenza tra F4V e MP4 sono i formati di metadati che F4V può memorizzare. Di seguito è riportato l'elenco dei formati di metadati supportati dal formato F4V.

- **Casella tag**: ulteriori quattro caselle tag opzionali (auth, title, dscp, cprt) all'interno della casella Movie (moov).
- **Casella metadati XMP**: questa casella arriva subito dopo la casella Film (moov). Con questo, il file può comunicare i metadati XMP a un filmato SWF tramite ActionScript.
- **prima casella**: questa casella si trova all'interno della casella Meta (meta) e può contenere un numero di tag di metadati. I tipi di dati supportati sono riportati di seguito.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Casella dei metadati della traccia del testo**: i campioni di testo (testo o tx3g) all'interno del Media Databox (mdat). Può contenere le seguenti caselle di metadati.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Riferimenti ##

- [Video Flash - Wikipedia](https://en.wikipedia.org/wiki/Video_Flash)

