---
date: 2020-08-12
keywords: jfif, .jfif, format file jfif, cara membuka file jfif, ekstensi .jfif, ekstensi jfif
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: File JFIF - Apa itu file .jfif?
linktitle: JFIF
description: "Pelajari tentang format file JFIF dan API yang dapat membuat dan membuka file JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Apa itu file JFIF?

JFIF (JPEG File Interchange Format (JFIF)) adalah file format gambar yang menggunakan ekstensi .jfif. JFIF dibangun di atas JIF (JPEG Interchange Format) dengan mengurangi kerumitan dan mengatasi keterbatasannya.

## Sejarah Singkat JFIF

Pengembangan dokumen JFIF dipimpin oleh Eric Hamilton dan kesepakatan tentang versi pertama ditetapkan pada akhir tahun 1991. Versi 1.02 diterbitkan pada tanggal 7 September 1992. RFC 2046 menetapkan bahwa format JFIF digunakan untuk mengirimkan gambar JPEG melalui internet. JFIF diterbitkan oleh ECMA pada tahun 2009 dan distandarisasi oleh ITU-T pada tahun 2011 sebagai Rekomendasi T.871 dan oleh ISO/IEC pada tahun 2013 sebagai ISO/IEC 10918-5

## Format File JFIF ##

File JFIF terdiri dari urutan penanda seperti yang didefinisikan di bagian 1 Standar JPEG. Setiap penanda terdiri dari dua byte (FF diikuti oleh sebuah byte yang menentukan jenis penanda). Penanda dapat berdiri sendiri atau menunjukkan awal segmen penanda.

JFIF memungkinkan banyak komponen seperti Y, Cb, Cr, untuk memiliki resolusi yang berbeda tetapi penyelarasannya tidak ditentukan. Tidak seperti JPEG, JFIF dapat memberikan informasi resolusi dan rasio aspek. JFIF juga menentukan model warna yang akan digunakan.

### Struktur Berkas ##

|Segmen|Kode|Deskripsi|
|---|---|---|
|SOI|FF D8|Awal Gambar|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segmen penanda tambahan|
|SOS|FF DA|Memulai Pemindaian|
||data gambar terkompresi||
|EOI|FF D9|Akhir Gambar|

Standar JFIF mendefinisikan segmen berikut:

### segmen penanda JFIF APP0 ###

Ini adalah segmen wajib yang berisi parameter gambar. Itu juga dapat berisi thumbnail tertanam yang tidak terkompresi.

|Bidang|Ukuran (byte)|Deskripsi|
|---|---|---|
|APP0 penanda|2|FF E0|
|Panjang|2|Panjang segmen tidak termasuk penanda APP0|
|Identifier|5|JFIF (4A 46 49 46 00) dalam ASCII diakhiri dengan null byte|
|Versi JFIF|2|Versi JFIF|
|Satuan kerapatan|1|Satuan untuk bidang kerapatan piksel berikut</br> 00 : Tidak ada satuan; rasio aspek lebar:tinggi piksel sama dengan Ydensity:Xdensity</br> 01 : Piksel per inci</br> 02 : Piksel per sentimeter|
|Xdensity|2|Kepadatan piksel horizontal lebih besar dari nol|
|Ydensity|2|Kepadatan piksel vertikal lebih besar dari nol|
|Xthumbnail|1|Jumlah piksel horizontal dari thumbnail RGB tersemat. Mungkin nol |
|Ythumbnail|1|Jumlah piksel vertikal dari thumbnail RGB tersemat. Mungkin nol |
|Data thumbnail|3 × n|Data thumbnail raster RGB 24 bit yang tidak terkompresi|

### segmen penanda APP0 ekstensi JFIF ###

Ini adalah bagian opsional yang jika ditentukan, harus segera mengikuti segmen penanda JFIF APP0. Bagian ini didukung oleh JFIF versi 1.02 ke atas dan memungkinkan penyematan thumbnail dalam tiga format berbeda.

|Bidang|Ukuran (byte)|Deskripsi|
|---|---|---|
|APP0 penanda|2|FF E0|
|Panjang|2|Panjang segmen tidak termasuk penanda APP0|
|Identifier|5|JFXX (4A 46 58 58 00) dalam ASCII diakhiri dengan null byte|
|Format thumbnail|1|Menentukan format data apa yang digunakan untuk thumbnail tersemat berikut:</br> 10 : Format JPEG</br> 11 : 1 byte per piksel format palet</br> 13 : 3 byte per piksel format RGB|
|Data thumbnail|variabel||

## Konversi JFIF ke Format File Gambar Lainnya

JFIF dapat dikonversi ke format file gambar populer seperti [PNG](/id/image/png/), [JPG](/id/image/jpg/), dan [PDF](/id/pdf/).

## Referensi ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

