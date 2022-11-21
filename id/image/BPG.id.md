---
date: 2020-08-12
keywords: bpg, .bpg, format file bpg, cara membuka file bpg, ekstensi .bpg, ekstensi bpg
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File BPG
linktitle: BPG
description: "Pelajari tentang format file BPG dan API yang dapat membuat dan membuka file BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Apa itu file BPG? ##

BPG (Better Portable Graphics) adalah format file yang dibuat oleh Fabrice Bellard pada tahun 2014 untuk gambar digital. Dia mengusulkan BPG sebagai pengganti JPEG karena BPG lebih efisien dalam kompresi atau ukuran. BPG menggunakan pengkodean intra-frame dari standar kompresi video HEVC (High-Efficiency Video Coding).

BPG dirancang sebagai format hemat memori portabel untuk bekerja pada perangkat genggam dan IoT. Saat ini, browser web tidak mendukung format BPG, tetapi situs web masih dapat menayangkan gambar BPG dengan menggunakan perpustakaan JavaScript yang ditulis oleh Bellard. BPG menggunakan profil Gambar Diam Utama 4:4:4 16 HEVC hingga 14 bit per sampel.

## Spesifikasi ##

Format wadah BPG adalah format gambar umum, bukan aliran bit mentah yang digunakan di HEVC. BPG mendukung format warna 4:4:4, 4:2:2, dan 4:2:0. Saluran alfa juga didukung dengan saluran ekstra berkode terpisah atau saluran keempat gambar CMYK. BPG menyediakan dukungan metadata untuk Exif, profil ICC, dan XMP. BPG mendukung YCbCr (ITU-R BT.601, BT.709, dan BT.2020 (pencahayaan non-konstan)), YCgCo, RGB, CMYK, dan ruang warna skala abu-abu. BGP juga mendukung animasi dan kompresi data HEVC lossy dan lossless.

## Referensi ##

- [Grafis Portabel Lebih Baik - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

