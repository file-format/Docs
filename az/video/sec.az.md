---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LSEC faylı yarada və aça bilən SEC fayl formatı və API-lər haqqında qazanıns.
title: SEC Fayl Format - Samsung Təhlükəsizlik Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## SEC faylı nədir?

SEC faylı Samsung DVR nəzarət sistemi ilə yaradılmış video fayldır. Video müşahidə kameralarından çəkilir və SEC formatında diskdə saxlanılır. Qeydə alınmış SEC videosu bir neçə kameradan video lenti idarə edə bilən Samsung-un video proqramı ilə oxuna bilər.

## SEC Fayl Format - Ətraflı Məlumat

SEC faylları xüsusi fayl formatından istifadə edərək daxilində h264/AVC axını ehtiva edir. SEC faylının başlığı SRD-1670D model nömrəsi ilə başlayır. Tarix və vaxt məlumatları faylın sonunda saxlanılır.

### SEC faylını AVI-yə çevirin

SEC faylı FFmpeg istifadə edərək standart [AVI](/video/avi/) fayl formatına çevrilə bilər.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## İstinadlar ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

