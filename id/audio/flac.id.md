---
date: 2019-12-13
keywords: flac, format file flac, ekstensi .flac, file flac, flac vs mp3
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file FLAC dan API yang dapat membuat dan membuka file FLAC."
title: Format File FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Apa itu file FLAC?

FLAC (Free Lossless Audio Codec) adalah format pengkodean audio kompresi lossless yang dikembangkan oleh Xiph.Org Foundation. FLAC adalah format terbuka bebas royalti yang disimpan dengan ekstensi .flac. Audio digital yang dikompresi menggunakan algoritme FLAC biasanya dikurangi ukurannya menjadi 50 hingga 70 persen. File FLAC dapat didekompresi menjadi salinan identik dari file audio asli.

## Format file FLAC

Ini adalah ikhtisar bitstream FLAC.

- **penanda fLaC**: Penanda ini ditambahkan ke awal streaming. Ini diikuti oleh satu atau lebih blok metadata.
- **Blok Metadata**: 128 jenis blok metadata didukung oleh FLAC; saat ini berikut ini didefinisikan.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Data audio terdiri dari satu atau beberapa frame audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Sejarah Singkat Format File FLAC

Josh Coalson memulai pengembangan FLAC pada tahun 2000. Versi pertama FLAC dirilis pada 20 Juli 2001. FLAC tergabung di bawah bendera Xiph.Org pada 20 Januari 2003. Pengembangan FLAC dipindahkan ke repositori git Xiph.Org dengan rilis versi 1.3.0 pada 26 Maret 2013.

## Komposisi Proyek FLAC

Proyek FLAC terdiri dari:

- Format aliran.
- Format wadah sederhana untuk aliran (FLAC).
- libFLAC: Pustaka encoder referensi, decoder, dan antarmuka metadata.
- libFLAC++: Pembungkus berorientasi objek untuk libFLAC.
- flac: Program baris perintah untuk menyandikan dan mendekode aliran FLAC.
- metaflac: Editor metadata baris perintah untuk FLAC.
- Plugin input untuk pemutar musik seperti Winamp, XMMX, dll.
- Format wadah Ogg (Ogg FLAC).

## Desain FLAC

Bergantung pada kepadatan dan amplitudo musik, ukuran file terkompresi bisa 80% lebih kecil dari file aslinya.

### Penyandi Sumber ###

- Ini hanya mendukung sampel integer dan bukan floating-point. Itu dapat menangani resolusi bit PCM dari 4 hingga 32 bit per sampel dan laju pengambilan sampel dari 1Hz hingga 65.535 Hz. Pengkodean FLAC dibatasi hingga 24 bit per sampel.
- Saluran dapat dikelompokkan untuk memanfaatkan korelasi antar saluran untuk meningkatkan kompresi.
- CRC checksum digunakan untuk mengidentifikasi frame yang rusak.
- Untuk konversi sampel audio, FLAC menggunakan prediksi linier.

### Metadata ###

- FLAC mendukung ReplayGain (digunakan untuk merasakan dan menormalkan kenyaringan dalam audio).
- FLAC menggunakan sistem yang sama dengan yang digunakan dalam komentar Vorbis untuk penandaan.
- libFLAC digunakan oleh sebagian besar aplikasi FLAC untuk encoding/decoding.
- libFLAC API diatur ke dalam aliran, aliran yang dapat dicari, dan file untuk meningkatkan abstraksi dari bitstream FLAC dasar.

### Kompresi ###

libFLAC menggunakan tingkat kompresi dari 0 hingga 8 di mana 0 adalah yang tercepat dan 8 adalah tingkat kompresi yang paling lambat. File terkompresi selalu lossless meskipun pengorbanannya antara kecepatan dan ukuran.

## FLAC vs MP3
MP3 adalah format kompresi lossy yang berarti dapat memotong sebagian audio untuk mengurangi ukurannya setelah menerapkan kompresi. Padahal, FLAC adalah format file lossless yang berarti Anda dapat mendengar audio dalam bentuknya yang paling murni. Sebelumnya format file lossless adalah CDA atau WAV yang tidak seefisien FLAC. Tabel berikut akan menunjukkan perbandingan antara kedua format ini untuk beberapa istilah penting:

|Jangka|FLAC|MP3|
---|---|---|
|**Kualitas Data**|Tidak ada kehilangan data audio| Beberapa data mungkin hilang saat mengompresi data audio|
|**Ukuran**|Ukuran file lebih besar dibandingkan dengan format lossy. Jadi butuh kapasitas penyimpanan yang lebih besar| Ukuran file lebih kecil, cocok diputar di perangkat audio ringkas dengan ruang penyimpanan kecil |
|**Persyaratan perangkat keras**| Butuh peralatan audio berkualitas tinggi dan kapasitas penyimpanan yang besar |Perpustakaan audio yang besar dapat disimpan di ruang penyimpanan yang lebih kecil. Cocok untuk perangkat genggam, seperti pemutar audio atau ponsel|
|**Pendistribusian melalui internet**|Tidak dapat didistribusikan dengan mudah melalui internet karena ukuran file yang besar |Ukuran file yang ringkas membuatnya mudah untuk didistribusikan melalui internet|
|**Kompatibilitas**|Codec mendengarkan musik dan audio paling populer yang cukup kompatibel dengan semua perangkat di planet iniKompatibel dengan PC generasi baru, ponsel, penerima AV, pemutar blu-ray, perangkat streaming seperti Roku atau Fire TV|

## Referensi ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

