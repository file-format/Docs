---
date: 2019-12-09
keywords: arc, .arc, format file arc, cara membuka file arc, ekstensi .arc, ekstensi arc
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File ARC
linktitle: ARC
description: "Pelajari tentang format file ARC dan API yang dapat membuat dan membuka file ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Apa itu file ARC?

ARC adalah kompresi data lossless dan format arsip yang dikembangkan oleh System Enhancement Associates (SEA). Format file dan aplikasi yang membuatnya disebut ARC. ARC sangat populer pada masa-masa awal BBS dial-up karena menggabungkan fitur kompresi dan pengarsipan banyak file dalam file yang sama. ARC kemudian digantikan oleh [ZIP](/id/compression/zip/) yang menawarkan rasio kompresi yang lebih baik.

Ekstensi file .arc digunakan oleh beberapa jenis file arsip yang tidak terkait seperti format ARC yang digunakan oleh Internet Archive untuk menyimpan banyak sumber daya web, format ARC berbeda yang digunakan oleh pengarsip FreeArc, format berbeda yang digunakan oleh Nintendo untuk sumber daya, dll. .

## Sejarah Singkat Format File ARC

Program ARC ditulis oleh Thom Henderson dari System Enhancement Associates pada tahun 1985. Program ini mengelompokkan file ke dalam satu file arsip dan juga mengompresnya. File yang dihasilkan oleh program ARC menggunakan ekstensi .arc. SEA merilis kode sumber untuk ARC pada tahun 1986 dan ARC dipindahkan ke Unix dan Atari ST oleh Howard Chu pada tahun 1987.

Phil Katz mengembangkan PKARC dan PKXARC untuk mengarsipkan dan mengekstrak file. File bekerja dengan format file ARC dan secara signifikan lebih cepat. Tidak seperti ARC, Katz membagi fungsi kompresi dan pengarsipan antara dua file berbeda yang mengurangi kebutuhan memori untuk menjalankannya.

Setelah gugatan antara SEA dan Katz, SEA menarik diri dari pasar shareware dan mengembangkan ARC+Plus dengan antarmuka pengguna layar penuh. Format ARC tidak lagi umum di PC.

## Format File ARC

File ARC terdiri dari urutan header file dan file yang diikuti oleh penanda akhir arsip seperti yang ditunjukkan di bawah ini.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Tajuk Berkas ARC ###

|Offset|Label|Jenis|Nilai|Deskripsi|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metode|
|02|ARCFNT|DS|12|namaberkas|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Ukuran terkompresi|
|13|ARCDAT|DW|0000|Tanggal berkas (MSDOS)|
|15|ARCTIM|DW|0000|Waktu file (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Ukuran tidak terkompresi|
|1D|ARCFIL|DS|ARCNSZ| |

### Metode Kompresi ###

Byte metode kompresi menunjukkan metode kompresi yang digunakan. Berikut ini adalah metode kompresi yang digunakan untuk file ARC.

|Metode|Nama|Deskripsi|
|---|---|---|
|0|Disimpan|Tidak ada kompresi yang digunakan|
|1|Dikemas|Enkode panjang lari berulang (RLE)|
|2|Diperas|Pengodean Huffman|
|3|Crunched|LZW dengan buffer 4K, kode 12 bit|
|4|Crunched|Packing pertama, lalu buffer LZW 4K dengan 12 bit|
|5|Crunched|Packing, LZW, buffer 4K, panjang variabel (9-12 bit)|
|6|Tergencet|LZW, buffer 8K, panjang variabel (9-13 bit)|
|7|Hancur|Packing, lalu buffer LZW 8K, 2-13 bit (PAK 1.0)|
|8|Saring|Huffman Dinamis dengan buffer 8K (PAK 2.0)|

## Referensi

- [ARC (format file) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

