---
date: 2022-01-06
keywords: vtt, .vtt, format file vtt, format file .vtt, ekstensi .vtt, ekstensi vtt
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Pelajari tentang file .vtt dan API yang dapat membuat dan membuka file VTT."
title: Format File VTT - File Trek Teks Video Web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Apa itu file VTT?

File VTT adalah file teks yang berisi informasi untuk menampilkan trek teks berwaktu (seperti subtitle atau keterangan) menggunakan format Trek Teks Video Web (WebVTT). Trek teks waktunya mencakup informasi seperti subtitel atau teks. Tujuan dari file VTT adalah untuk menambahkan overlay teks ke a<video> . Formatnya agak mirip dengan file SRT. File teks berbasis WebVTT dikodekan menggunakan UTF-8. File VTT berisi informasi seperti subtitle, deskripsi, keterangan, deskripsi, bab, dan metadata. Menjadi file teks biasa, file VTT dapat dibuka menggunakan editor teks seperti Microsoft Notepad, Apple TextEdit, dan Notepad++.

## Format File VTT - Informasi lebih lanjut

File VTT menggunakan format file WebVTT untuk menyimpan informasi trek teks berurutan. Setiap trek teks berwaktu terdiri dari satu baris atau beberapa baris, juga dikenal sebagai `isyarat` seperti yang ditampilkan dalam contoh berikut.

### Contoh Berkas VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Struktur Berkas VTT

Berikut ini adalah persyaratan struktur file VTT.

* Tanda pesanan byte opsional (BOM).
* Baris "WEBVTT".
* Sebuah header teks opsional di sebelah kanan WEBVTT.
* Baris kosong, yang setara dengan dua baris baru berturut-turut.
* Nol atau lebih isyarat atau komentar.
* Nol atau lebih baris kosong.

## Referensi

* [VTT - Sekolah W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

