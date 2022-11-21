---
date: 2019-10-11
keywords: srt, .srt, format file srt, format file .srt, ekstensi .srt, ekstensi srt
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file SRT dan API yang dapat membuat dan membuka file SRT."
title: Format File SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Apa itu file SRT? ##

SRT (format file SubRip) adalah file subtitle sederhana yang disimpan dalam format file SubRip dengan ekstensi .srt. Ini berisi sejumlah subtitle berurutan, stempel waktu mulai dan berakhir, dan teks subtitle. File SRT memungkinkan untuk menambahkan subtitle ke konten video setelah diproduksi.

## Struktur file SRT ##

Setiap subtitle memiliki empat bagian dalam file SRT.

1. Penghitung angka yang menunjukkan nomor atau posisi teks film.
1. Waktu awal dan akhir subtitle dipisahkan oleh --> karakter
1. Teks subtitle dalam satu baris atau lebih.
1. Baris kosong yang menunjukkan akhir subjudul.

### Contoh SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Untuk menentukan waktu *jam:menit:detik,milidetik (00:00:00,000)* digunakan format.

## Memformat file SRT ##

Pemformatan file SRT berasal dari tag HTML. Tag pemformatan untuk file SRT tercantum di bawah ini.

| Efek | Tag |
| --- | --- |
|Bold|**\ <b>...\</b> ** atau {b}...{/b}|
|Italik|**\ <i>...\</i> ** atau **{i}...{/i}**|
|Underline|**\ <u>...\</u> ** atau **{u}...{/u}**|
|Warna Huruf|**\ <font color="white">...\</font> **|
|Posisi Baris|**{\a3}** (menunjukkan bahwa teks akan mulai muncul pada baris 3)

## Perangkat Lunak SubRip ##

SubRip adalah program perangkat lunak gratis yang berjalan di Windows. Ini mengekstrak subtitle dan waktunya dari berbagai format video dan menyimpan subtitle dalam format SRT. SubRip menggunakan pengenalan karakter optik untuk mengekstrak subtitle dari video langsung, file video lain, dan DVD.

## Referensi ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
