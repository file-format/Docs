---
date: 2019-10-11
keywords: flv, .flv, format file flv, format file .flv, ekstensi .flv, ekstensi flv, format video flv
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file FLV dan API yang dapat membuat dan membuka file FLV."
title: Format File FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Apa itu file FLV? ##

FLV (Flash Video) adalah format file kontainer dengan ekstensi .flv. FLV digunakan untuk mengirimkan konten audio/video melalui internet dengan menggunakan Adobe Flash Player atau Adobe Air. Data dalam file FLV dikodekan dengan cara yang sama seperti file SWF. Dukungan langsung ditambahkan ke Flash Player 7 pada tahun 2003. Sistem Adobe membuat F4V pada tahun 2007 karena pembatasan FLV.

### Pengkodean ###

File FLV berisi bitstream video dari Sorenson Spark yang merupakan varian eksklusif dari standar video H.263. Ini adalah format kompresi yang diperlukan untuk Flash Player 6 dan 7. Versi 8 dari Flash Player mendukung bitstream video On2 TrueMotion VP6. Ini adalah format kompresi yang direkomendasikan untuk Flash Player 8 dan lebih tinggi. FLV mendukung audio dalam MP3, Nellymoser Asao Codec, dan codec Speex open-source. Ini juga mendukung audio format ADPCM atau audio yang tidak terkompresi. AAC (HE-AAC/AAC SBR, AAC Main Profile, dan AAC-LC) didukung oleh Flash Player 9 versi terbaru.

## Struktur ##

File FLV terdiri dari Header dan Packet. File FLV dimulai dengan Header. Header memiliki bidang-bidang berikut.

- **Signature**: Nilainya adalah FLV
- **Versi**: Nilai standarnya adalah 1. Hanya 0x01 yang valid.
- **Bendera**: 0x04 digunakan untuk audio dan 0x01 digunakan untuk video sehingga 0x05 digunakan untuk audio dan video.
- **Ukuran Header**: Nilai defaultnya adalah 9. Ini digunakan untuk melewati header baru yang diperluas.

Setelah header muncul Paket. File FLV dibagi menjadi beberapa paket yang disebut tag FLV yang memiliki header 15-byte. Paket berisi metadata untuk audio, video, skrip, informasi enkripsi, dan payload. Paket FLV memiliki bidang-bidang berikut.

- **Dicadangkan**: Dicadangkan untuk FMS dan harus 0.
- **Filter**: Menunjukkan apakah paket difilter atau tidak.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Jenis Paket**: Ini menentukan jenis konten dalam paket.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Ukuran Data**: Ini menunjukkan panjang pesan.
- **Timestamp Lower**: Ini menyimpan timestamp dalam milidetik saat data tag berlaku. Ini diatur ke NULL untuk paket pertama.
- **Timestamp Upper**: Ekstensi untuk membuat nilai uint32_be.
- **Stream ID**: Ini disetel ke NULL untuk streaming pertama.
- **Data Muatan**: Ini adalah data berdasarkan jenis paket.

## Referensi ##

- [Video Flash - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

