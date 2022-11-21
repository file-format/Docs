---
date: 2019-12-09
keywords: arj, .arj, format file arj, cara membuka file arj, ekstensi .arj, ekstensi arj
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File ARJ
linktitle: ARJ
description: "Pelajari tentang format file ARJ dan API yang dapat membuat dan membuka file ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Apa itu file ARJ? ##

ARJ (Diarsipkan oleh Robert Jung) adalah file arsip terkompresi efisiensi tinggi yang dikembangkan oleh Robert K. Jung. ARJ dikembangkan untuk DOS dan versi awal Windows pada awal 1990-an. File ARJ berguna untuk mencadangkan atau berbagi file dalam jumlah besar karena Anda tidak perlu melacak semua file tersebut dan hanya ada satu file yang harus ditangani. Ekstensi .arj digunakan untuk file arsip ARJ.

## Format File ARJ ##

File ARJ berisi dua jenis header:

- Header utama: Ada satu header utama di awal arsip.
- Header lokal: Header lokal ada sebelum setiap file.

|Offset|Tipe|Hitung|Deskripsi|
|---|---|---|---|
|0000h|kata|1|ID=0EA60h|
|0002h|kata|1|ukuran tajuk dasar|
|0004h|byte|1|Ukuran tajuk|
|0005h|byte|1|Nomor versi pengarsip|
|0006h|byte|1|Diperlukan nomor versi minimum|
|0007h|bita|1|OS Inang:</br> 0 - MS-DOS</br> 1 - PRIMO</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Sistem xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - Selanjutnya</br> 9 - VAX VMS|
|0008h|byte|1|Bendera Internal, dipetakan:</br> 0 - tanpa kata sandi / kata sandi</br> 1 - dipesan</br> 2 - file berlanjut di disk berikutnya</br> 3 - bidang posisi awal file tersedia</br> 4 - terjemahan jalur ( "\" ke "/" )|
|0009h|byte|1|Metode kompresi:</br> 0 - disimpan</br> 1 - paling banyak dikompresi</br> 2 - dikompresi</br> 3 - dikompresi lebih cepat</br> 4 - tercepat terkompresi|
|000Ah|bita|1|Tipe berkas:</br> 0 - biner</br> 1 - teks 7-bit</br> 2 - tajuk komentar</br> 3 - direktori</br> 4 - label volume|
|000Bh|byte|1|dicadangkan|
|000Ch|dword|1|Tanggal/Waktu file asli dalam format MS-DOS|
|0010h|dword|1|Ukuran file terkompresi|
|0014h|kata sandi|1|Ukuran file asli"|
|0018h|kata sandi|1|CRC-32 dari file asli|
|001Ah|kata|1|Posisi spesifikasi file dalam nama file|
|001Ch|kata|1|Atribut file|
|001Eh|kata|1|Data host|
|?|Dword|1|Perpanjangan posisi awal file|
|????h|dword|1|CRC-32 dari header dasar|
|????h|kata|1|Ukuran dari header yang diperluas pertama|
|????h+"SIZ"+2|dword|1|CRC-32 dari header tambahan|
|????h+"SIZ"+6|byte|?|Berkas terkompresi|

## Referensi ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

