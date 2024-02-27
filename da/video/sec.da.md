---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltjene om SEC filformat og API'er, der kan oprette og åbne SEC fils.
title: SEC-filformat - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Hvad er SEC fil?

En SEC-fil er en videofil, der er oprettet med Samsung DVR-overvågningssystem. Video optages fra overvågningskameraer og gemmes på disk i SEC-format. Den optagede SEC-video kan afspilles med Samsungs videosoftware, der kan styre videofeed fra flere kameraer.

## SEC-filformat - flere oplysninger

SEC-filer indeholder h264/AVC-stream inde ved hjælp af proprietært filformat. Overskriften på en SEC-fil starter med modelnummeret på SRD-1670D. Oplysningerne om dato og klokkeslæt opbevares i slutningen af filen.

### Konverter SEC-fil til AVI

SEC-filen kan konverteres til standardfilformatet [AVI](/video/avi/) ved hjælp af FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referencer ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

