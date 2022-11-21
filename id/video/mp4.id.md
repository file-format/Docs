---
date: 2019-10-11
keywords: MP4, file, ekstensi, format, format video, MPEG-4
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file MP4 dan API yang dapat membuat dan membuka file MP4."
title: Berformat File MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Apa itu berkas MP4? ##

MP4 (kependekan dari MPEG-4 Bagian 14) adalah format file berdasarkan ISO/IEC 14496-12:2004 yang didasarkan pada QuickTime File Format tetapi secara resmi menentukan dukungan untuk Initial Object Descriptors (IOD) dan fitur MPEG lainnya. Sebagian besar digunakan untuk menyimpan video dan audio tetapi juga dapat digunakan untuk menyimpan subtitle dan gambar diam. File MP4 disimpan dengan ekstensi .mp4. MP4 adalah standar pengkodean audio-visual internasional. Mirip dengan sebagian besar format wadah modern, MP4 mendukung streaming melalui internet. Karena kompresi tinggi yang digunakan dalam MP4, file yang dihasilkan berukuran lebih kecil dengan hampir semua kualitas aslinya dipertahankan.

## Sejarah Singkat ##

Spesifikasi MP4 dikembangkan oleh Moving Picture Experts Group (MPEG) dan didasarkan pada format QuickTime [MOV](/id/video/mov/) yang diterbitkan pada tahun 2001. Versi pertama (ISO/IEC 14496-1:2001) MP4 adalah revisi dari MPEG-4 Bagian 1: Spesifikasi sistem yang diterbitkan pada tahun 1999. Format file MP4 digeneralisasikan ke Format File Media Berbasis ISO ISO/IEC 14496-12:2004 yang menentukan struktur umum untuk file media berbasis waktu. Akibatnya, ini digunakan sebagai dasar untuk format file lainnya.

## Struktur File MP4 ##

MP4 adalah file wadah yang dapat diperluas, artinya tidak menentukan struktur yang ketat dan memungkinkan struktur dan hierarki khusus untuk setiap jenis media. Data dalam file MP4 dibagi menjadi dua bagian, yang pertama berisi data terkait media dan yang kedua berisi metadata. Data media berisi audio atau video dan metadata menunjukkan tanda untuk akses acak, stempel waktu, dll.
Struktur dalam MP4 biasanya disebut sebagai atom atau kotak. Ukuran minimum atom adalah 8 byte (4 byte pertama menentukan ukuran dan 4 byte berikutnya menentukan jenis). Berikut adalah daftar atom level root yang terkandung dalam file MP:

- **ftyp**: Berisi jenis file, deskripsi, dan struktur data umum yang digunakan.
- **pdin**: Berisi informasi pemuatan/pengunduhan video progresif.
- **moov**: Penampung untuk semua metadata film.
- **moof**: Penampung dengan fragmen video.
- **mfra**: Wadah dengan akses acak ke fragmen video
- **mdat**: Penampung data untuk media.
- **stts**: tabel sampel ke waktu.
- **stsc**: tabel sample-to-chunk.
- **stsz**: ukuran sampel (pembingkaian)
- **meta**: Wadah dengan informasi metadata.

Berikut adalah daftar atom tingkat kedua yang digunakan dalam MP4:

- **mvhd**: Berisi informasi header video dengan detail lengkap video.
- **trak**: Kontainer dengan trek individual.
- **udta**: Wadah dengan informasi pengguna dan trek.
- **iods**: deskriptor file MP4

## Referensi ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

