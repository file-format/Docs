---
date: 2022-03-25
keywords: sec, .sec, sec dosya biçimi, .sec dosya biçimi, .sec uzantısı, sec uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "SEC dosya formatı ve SEC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: SEC Dosya Biçimi - Samsung Güvenlik Video Dosyası
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## SEC dosyası nedir?

SEC dosyası, Samsung DVR gözetim sistemi ile oluşturulan bir video dosyasıdır. Video, güvenlik kameralarından yakalanır ve SEC formatında diske kaydedilir. Kaydedilen SEC videosu, Samsung'un birden fazla kameradan gelen video beslemesini yönetebilen video yazılımıyla oynatılabilir.

## SEC Dosya Biçimi - Daha Fazla Bilgi

SEC dosyaları, tescilli dosya formatını kullanarak içinde h264/AVC akışı içerir. Bir SEC dosyasının başlığı, SRD-1670D'nin model numarasıyla başlar. Tarih ve saat bilgisi dosyanın sonunda tutulur.

### SEC Dosyasını AVI'ye Dönüştür

SEC dosyası, FFmpeg kullanılarak standart [AVI](/tr/video/avi/) dosya formatına dönüştürülebilir.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referanslar ##

- [Samsung ve SEC Dosyaları](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

