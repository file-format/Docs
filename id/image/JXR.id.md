---
date: 2020-08-12
keywords: jxr, .jxr, format file jxr, cara membuka file jxr, ekstensi .jxr, ekstensi jxr
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File JXR
linktitle: JXR
description: "Pelajari tentang format file JXR dan API yang dapat membuat dan membuka file JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Apa itu file JXR? ##

JPEG XR (JPEG extended range) adalah format file untuk gambar fotografi nada kontinu. Ini adalah standar kompresi gambar diam yang didasarkan pada Foto HD yang dikembangkan oleh Microsoft. Ini mendukung kompresi lossy dan lossless.

## Sejarah Singkat ##

Windows Media Photo pertama kali diumumkan oleh Microsoft di WinHEC 2006. Ia berganti nama menjadi HD Photo pada November 2006. JPEG XR disetujui sebagai Standar Internasional ISO/IEC 29199-2 pada 19 Juni 2009. ITU-T dan ISO/IEC menerbitkan mosi spesifikasi format (ITU-T T.833 | ISO/IEC 29199-3), perangkat uji kesesuaian (ITU-T T.834 | ISO/IEC 29199-4), dan perangkat lunak referensi (ITU-T T.835 | ISO /IEC 29199-5) untuk JPEG XR setelah selesainya spesifikasi pengkodean gambar pada tahun 2010. Laporan teknis yang menjelaskan arsitektur alur kerja untuk JPEG XR diterbitkan pada tahun 2011.

## Desain JPEG XR ##

Dibandingkan dengan JPEG, JPEG XR menawarkan beberapa peningkatan termasuk:

- **Kompresi Lebih Baik**: JPEG XR menawarkan rasio kompresi lebih tinggi.
- **Kompresi Lossless**: JPEG XR mendukung kompresi lossless.
- **Struktur Petak**: Gambar JPEG XR dapat disegmentasi ke dalam wilayah petak di mana setiap wilayah dapat didekodekan secara terpisah.
- **Lebih akurat warna**: JPEG XR menyertakan konversi internal ke ruang warna YCoCg untuk mendukung gambar menggunakan ruang warna RGB. JPEG XR juga mendukung model warna CMYK integer 16-bit per komponen (64-bit per piksel). JPEG XR mendukung format warna floating point eksponen bersama RGBE untuk gambar HDR. JPEG XR juga mendukung pengkodean warna skala abu-abu dan multi-saluran.
- **Peta Transparansi**: JPEG XR mendukung saluran alfa untuk transparansi.
- **Modifikasi gambar domain terkompresi**: Gambar JPEG XR dapat dikonversi menjadi pengkodean lossy, resolusi dikurangi, dipotong, dibalik, diputar, dan struktur petak dapat diubah semua tanpa decoding penuh file.
- **Dukungan Metadata**: File gambar JPEG XR mungkin berisi profil warna ICC untuk representasi warna yang konsisten di beberapa perangkat. Format ini juga mendukung format metadata Exif dan XMP.

## Format Wadah ##

Data gambar JPEG XR dapat disimpan dalam format wadah mirip TIFF dengan menggunakan tabel tag Image File Directory (IFT). File JXR berisi yang berikut ini dalam tag IFD:

- Data gambar: Ini adalah data gambar mandiri yang berdekatan.
- Data saluran alfa opsional: Jika ini ada, data gambar dapat dikompresi secara terpisah dengan mengaktifkan dukungan aplikasi yang tidak mendukung transparansi.
- Metadata
- Metadata XMP opsional
- Metadata Exif opsional

Karena didasarkan pada format TIFF, ini mewarisi semua batasan format TIFF seperti batas ukuran file 4 GB.

## Referensi ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

