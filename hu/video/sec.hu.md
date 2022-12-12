---
date: 2022-03-25
keywords: sec, .sec, sec fájlformátum, .sec fájlformátum, .sec kiterjesztése, mp kiterjesztése
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Ismerje meg a SEC fájlformátumot és az API-kat, amelyek SEC-fájlokat hozhatnak létre és nyithatnak meg."
title: SEC fájlformátum – Samsung biztonsági videófájl
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Mi az a SEC fájl?

A SEC fájl egy videofájl, amelyet a Samsung DVR felügyeleti rendszerrel hoztak létre. A videót a térfigyelő kamerák rögzítik, és SEC formátumban lemezre tárolják. A rögzített SEC-videót a Samsung videoszoftverével lehet lejátszani, amely képes kezelni több kamera videofeedjét.

## SEC fájlformátum – További információ

A SEC fájlok h264/AVC adatfolyamot tartalmaznak belül szabadalmaztatott fájlformátumban. A SEC fájl fejléce az SRD-1670D modellszámával kezdődik. A dátum és idő információ a fájl végén található.

### A SEC fájl konvertálása AVI formátumba

A SEC fájl az FFmpeg segítségével a szabványos [AVI](/hu/video/avi/) fájlformátumba konvertálható.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referenciák ##

- [Samsung és SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

