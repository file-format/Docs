---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lnopelniet par SEC faila formātu un API, kas var izveidot un atvērt SEC failus.
title: SEC faila formāts — Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Kas ir SEC fails?

SEC fails ir video fails, kas izveidots ar Samsung DVR novērošanas sistēmu. Video tiek uzņemts no novērošanas kamerām un saglabāts diskā SEC formātā. Ierakstīto SEC video var atskaņot, izmantojot Samsung video programmatūru, kas var pārvaldīt video plūsmu no vairākām kamerām.

## SEC faila formāts — vairāk informācijas

SEC faili satur h264/AVC straumi iekšpusē, izmantojot patentētu faila formātu. SEC faila galvene sākas ar SRD-1670D modeļa numuru. Datuma un laika informācija tiek glabāta faila beigās.

### Konvertējiet SEC failu uz AVI

SEC failu var pārveidot standarta [AVI](/video/avi/) faila formātā, izmantojot FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Atsauces Nr.

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

