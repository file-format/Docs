---
date: 2019-10-11
keywords: f4v, .f4v, format file f4v, format file .f4v, ekstensi .f4v, ekstensi f4v, format video f4v, cara membuka file f4v, apa itu file f4v
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file F4V dan API yang dapat membuat dan membuka file F4V"
title: Format File F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Apa itu file F4V? ##

F4V (Flash MP4 Video File) adalah file video yang disimpan dengan ekstensi .f4v. Ini didasarkan pada format file media dasar ISO (MPEG-4 Bagian 12). Ini sangat mirip dengan [MP4](/id/video/mp4/) oleh karena itu juga disebut sebagai Flash MP4 secara informal. [FLV](/id/video/flv/) memiliki keterbatasan saat streaming konten H.264/ACC yang mengakibatkan Adobe Systems membuat format F4V baru. Flash Player dapat memutar file F4V sejak rilis Flash Player 9 Update 3.

## Struktur file F4V ##

Format file F4V didasarkan pada format file media dasar ISO (MPEG-4 Bagian 12) dan sangat mirip dengan format MP4. Untuk detail mengenai struktur, silakan lihat halaman [MP4](/id/video/mp4/). Perbedaan utama antara F4V dan MP4 adalah format metadata yang dapat disimpan oleh F4V. Diberikan di bawah ini adalah daftar format metadata yang didukung oleh format F4V.

- **Kotak tag**: Tambahan empat kotak tag opsional (auth, title, dscp, cprt) di dalam kotak Movie (moov).
- **Kotak Metadata XMP**: Kotak ini berada tepat setelah kotak Film (moov). Dengan ini, file dapat mengomunikasikan metadata XMP ke film SWF melalui ActionScript.
- **kotak pertama**: Kotak ini muncul di dalam kotak Meta (meta) dan dapat berisi sejumlah tag metadata. Jenis data yang didukung diberikan di bawah ini.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Kotak Metadata Trek Teks**: Sampel teks (teks atau tx3g) di dalam Media Databox (mdat). Itu dapat berisi kotak metadata berikut.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referensi ##

- [Video Flash - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

