---
date: 2021-03-21
keywords: alac, format file alac, ekstensi .alac
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Pelajari tentang format file ALAC dan API yang dapat membuat dan membuka file ALAC."
title: ALAC - Format File Codec Audio Lossless Apple
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Apa itu file ALAC?

Format file ALAC adalah Apple Lossless Audio Codec (ALAC) yang menggunakan wadah QuickTime yang sesuai dengan MPEG-4. Itu diperkenalkan pada tahun 2004 sebagai format file berpemilik, hingga 2011 ketika Apple membuatnya tersedia open source dan bebas royalti. Formatnya mirip dengan [FLAC](/id/audio/flac/) (Free Lossless Audio Codec) tetapi menawarkan lebih banyak kompresi secara komparatif. Ini menawarkan alternatif suara yang lebih baik untuk [AAC](/id/audio/aac/) atau [MP3](/id/audio/mp3/). File audio yang disandikan dengan codec ALAC dapat dibuka menggunakan Apple QuickTime, Apple iTunes, dan Micrsoft Windows Media Player dengan codec K-Lite.

## Format File ALAC

File berdasarkan codec ALAC adalah file biner yang tersedia sebagai [sumber terbuka di GitHub](https://github.com/macosforge/alac) untuk referensi pengembang. Ini berisi sumber untuk encoder dan decoder ALAC. Apple juga telah menyediakan utilitas baris perintah, yang disebut `alacconvert`, untuk membaca dan menulis data audio ke/dari file Core Audio Format (CAF) dan [WAVE](/id/audio/wav/). Berikut adalah beberapa poin penting tentang format file ALAC.

1. `Kedalaman Bit` - 16, 20, 24, dan 32 bit.
1. `Sample Rate` - Tingkat sampel bilangan bulat arbitrer apa pun dari 1 hingga 384.000 Hz. Kecepatan teoretis hingga 4.294.967.295 (2^32 - 1) Hz dapat didukung.
1. `Ukuran Paket` - Ukuran paket default default ke 4096 sampel frame audio per paket. Ukuran paket lain tentu saja memungkinkan. Namun, ukuran paket non-default tidak dijamin berfungsi dengan baik di semua perangkat keras yang mendukung Apple Lossless. Paket di atas 16.384 kerangka sampel tidak didukung.
1. `Saluran yang Didukung` - Ini mendukung satu hingga delapan saluran. Setiap saluran memiliki urutan informasi berikut.

|Num Chan| Pesan|
|---|---|
|1 |mono|
|2 |stereo (Kiri, Kanan)|
|3 |MPEG 3.0 B (Tengah, Kiri, Kanan)|
|4 |MPEG 4.0 B (Tengah, Kiri, Kanan, Tengah Sekitar)|
|5 |MPEG 5.0 D (Tengah, Kiri, Kanan, Surround Kiri, Surround Kanan)|
|6 |MPEG 5.1 D (Tengah, Kiri, Kanan, Surround Kiri, Surround Kanan, Efek Frekuensi Rendah)|
|7 |Apple AAC 6.1 (Tengah, Kiri, Kanan, Surround Kiri, Surround Kanan, Surround Tengah, Efek Frekuensi Rendah)|
|8 |MPEG 7.1 B (Tengah, Tengah Kiri, Tengah Kanan, Kiri, Kanan, Surround Kiri, Surround Kanan, Efek Frekuensi Rendah)|

## Referensi

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac di GitHub](https://github.com/macosforge/alac)

