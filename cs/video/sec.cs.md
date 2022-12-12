---
date: 2022-03-25
keywords: sek, .sec, formát souboru sec, formát souboru .sec, přípona .sec, přípona sek
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o formátu souboru SEC a rozhraních API, která mohou vytvářet a otevírat soubory SEC."
title: Formát souboru SEC – Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Co je soubor SEC?

Soubor SEC je soubor videa, který je vytvořen pomocí monitorovacího systému Samsung DVR. Video je zachycováno z monitorovacích kamer a ukládáno na disk ve formátu SEC. Zaznamenané SEC video lze přehrát pomocí video softwaru Samsung, který dokáže spravovat video z více kamer.

## Formát souboru SEC – Další informace

Soubory SEC obsahují proud h264/AVC uvnitř pomocí proprietárního formátu souboru. Záhlaví souboru SEC začíná číslem modelu SRD-1670D. Informace o datu a čase jsou uloženy na konci souboru.

### Převést soubor SEC do AVI

Soubor SEC lze převést do standardního formátu souboru [AVI](/cs/video/avi/) pomocí FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Reference ##

- [Soubory Samsung a SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

