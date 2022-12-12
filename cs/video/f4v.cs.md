---
date: 2019-10-11
keywords: f4v, .f4v, formát souboru f4v, formát souboru .f4v, přípona .f4v, přípona f4v, formát videa f4v, jak otevřít soubory f4v, co jsou soubory f4v
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souborů F4V a rozhraních API, která mohou vytvářet a otevírat soubory F4V"
title: Formát souboru F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Co je soubor F4V? ##

F4V (Flash MP4 Video File) je video soubor uložený s příponou .f4v. Je založen na základním formátu mediálního souboru ISO (MPEG-4 část 12). Je velmi podobný [MP4](/cs/video/mp4/), proto se také neformálně označuje jako Flash MP4. [FLV](/cs/video/flv/) měl omezení při streamování obsahu H.264/ACC, což vedlo k tomu, že společnost Adobe Systems vytvořila nový formát F4V. Flash Player může přehrávat soubory F4V od vydání aktualizace Flash Player 9 Update 3.

## Struktura souborů F4V ##

Formát souboru F4V je založen na základním formátu mediálního souboru ISO (MPEG-4 Part 12) a je velmi podobný formátu MP4. Podrobnosti týkající se struktury naleznete na stránce [MP4](/cs/video/mp4/). Hlavním rozdílem mezi F4V a MP4 jsou formáty metadat, které může F4V ukládat. Níže je uveden seznam formátů metadat podporovaných formátem F4V.

- **Tag box**: Další čtyři volitelná pole tagů (auth, title, dscp, cprt) v poli Movie (moov).
- **Pole metadat XMP**: Toto pole se nachází hned za polem Film (moov). Díky tomu může soubor předávat metadata XMP k filmu SWF prostřednictvím jazyka ActionScript.
- **ilst box**: Toto pole se nachází uvnitř pole Meta (meta) a může obsahovat řadu značek metadat. Podporované datové typy jsou uvedeny níže.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata box**: Textové vzorky (text nebo tx3g) uvnitř Media Databox (mdat). Může obsahovat následující pole metadat.
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

## Reference ##

- [Flash Video - Wikipedie](https://en.wikipedia.org/wiki/Flash_Video)

