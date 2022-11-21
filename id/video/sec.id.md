---
date: 2022-03-25
keywords: detik, .sec, format file detik, format file .sec, ekstensi .sec, ekstensi detik
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Pelajari tentang format file SEC dan API yang dapat membuat dan membuka file SEC."
title: Format File SEC - File Video Keamanan Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Apa itu file SEC?

File SEC adalah file video yang dibuat dengan sistem pengawasan Samsung DVR. Video diambil dari kamera pengintai dan disimpan ke disk dalam format SEC. Video SEC yang direkam dapat diputar ulang dengan perangkat lunak video Samsung yang dapat mengelola umpan video dari beberapa kamera.

## Format File SEC - Informasi Lebih Lanjut

File SEC berisi aliran h264/AVC di dalamnya menggunakan format file berpemilik. Header file SEC dimulai dengan nomor model SRD-1670D. Informasi tanggal dan waktu disimpan di akhir file.

### Konversi File SEC ke AVI

File SEC dapat dikonversi ke format file [AVI](/id/video/avi/) standar menggunakan FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referensi ##

- [File Samsung dan SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

