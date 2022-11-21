---
date: 2019-10-11
keywords: rm, .rm, format file rm, format file .rm, ekstensi .rm, format file RealMedia
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file RM dan API yang dapat membuat dan membuka file RM."
title: Format File RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Apa itu file RM? ##

RealMedia adalah format wadah multimedia berpemilik yang dikembangkan oleh RealNetworks yang menggunakan ekstensi .rm. Ini digunakan dengan kombinasi [RealAudio (RA)](/id/audio/ra/) dan [RealVideo(RV)](/id/video/rv/) untuk streaming melalui internet. Aliran ini memiliki bitrate konstan. Untuk kecepatan bit variabel, RealNetworks mengembangkan format RealMedia Variable Bitrate (RMVB). RealMedia cocok untuk streaming konten melalui internet dan bisa digunakan untuk streaming siaran langsung televisi misalnya.

## Struktur File RealMedia ##

File RealMedia terdiri dari serangkaian potongan, masing-masing memiliki struktur berikut:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Berikut ini adalah jenis potongan yang ada di file RealMedia:

- **RealMedia file header (.RMF)**: Ini harus menjadi potongan pertama dalam file RealMedia. Hanya satu potongan RMF yang ada dalam satu file. Ini berisi informasi tentang jumlah header.
- **File properties header (PROP)**: Berisi informasi tentang properti umum file RealMedia. Hanya ada satu potongan jenis ini di setiap file RealMedia.
- **Media properties header (MDPR)**: Potongan ini berisi informasi tentang properti stream. Ini berisi informasi tentang jenis aliran dan codec yang digunakan. Ada satu potongan MDPR untuk setiap aliran dalam file.
- **Content description header (CONT)**: Potongan ini berisi informasi teks seperti judul atau pengarang untuk konten di file RealMedia. Potongan ini hanya untuk tujuan informasi.
- **Data header (DATA)**: Potongan ini berisi sekelompok paket data.
- **Index header (INDX)**: Potongan ini muncul setelah semua potongan DATA dan berisi entri indeks. Satu file dapat memiliki lebih dari satu potongan INDX.

## Format audio dan video yang didukung ##

### Format audio ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
-dnet: AC3
- sipr: sipro
- masak: Masak
-atrc: ATRAC3
- ralf: Format RealAudio Lossless
- raac: LC-AAC
- rak: HE-AAC

### Format video ###

- CLV1: Hapus Video
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: pendahulu H.264
- RV40: prekursor H.264, RV40
-RVTR: H.263+ (RV20)

## Referensi ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

