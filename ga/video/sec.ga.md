---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid CSS agus APIs ar féidir leo comhad CSS a chruthú agus a oscailts.
title: SFormáid Comhaid CE - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Cad is comhad CSS ann?

Is comhad físe é comhad CSS a chruthaítear le córas faireachais Samsung DVR. Gabhtar físeán ó cheamaraí faireachais agus stóráiltear é chuig diosca i bhformáid CSS. Is féidir an físeán SEC taifeadta a sheinm ar ais le bogearraí físe Samsung ar féidir leo fotha físeáin ó ilcheamaraí a bhainistiú.

## Formáid Chomhaid SEC - Tuilleadh Eolais

Tá sruth h264/AVC istigh i gcomhaid CSS ag baint úsáide as formáid comhaid dílseánaigh. Tosaíonn ceanntásc comhaid CSS le huimhir mhúnla an SRD-1670D. Coinnítear an fhaisnéis dáta agus ama ag deireadh an chomhaid.

### Tiontaigh SEC Comhad go AVI

Is féidir comhad SEC a thiontú go formáid comhaid chaighdeánach [AVI](/video/avi/) le FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Tagairtí ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

