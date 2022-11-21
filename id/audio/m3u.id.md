---
date: 2019-12-13
keywords: m3u, format file m3u, ekstensi .m3u, daftar putar multimedia m3u, format daftar putar m3u
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file M3U dan API yang dapat membuat dan membuka file M3U."
title: Format File M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Apa itu file M3U? ##

M3U (URL MP3) adalah file daftar putar audio yang disimpan dengan ekstensi .m3u. M3U bukan file audio yang sebenarnya, itu hanya menunjuk ke file audio dan terkadang video. M3U dikembangkan untuk digunakan dengan perangkat lunak Winplay3 oleh Fraunhofer. Itu juga didukung oleh berbagai pemutar media dan perangkat lunak.

## Format File M3U

Tidak ada spesifikasi resmi untuk format file M3U, ini adalah standar de-facto. M3U adalah file teks biasa yang menggunakan ekstensi .m3u jika teks dikodekan dalam pengkodean non-Unicode default sistem lokal atau dengan ekstensi .m3u8 jika teks dikodekan UTF-8. Setiap entri dalam file M3U dapat menjadi salah satu dari berikut ini:

- Jalur absolut ke file
- Jalur file relatif ke file M3U.
- URL

### M3U yang diperluas ###

Di M3U yang diperluas, arahan tambahan diperkenalkan yang dimulai dengan "#" dan diakhiri dengan titik dua (:) jika mereka memiliki parameter. Diberikan di bawah ini adalah daftar arahan untuk diperpanjang M3U.

- **#EXTM3U** - Ini adalah header file yang menunjukkan Extended M3U dan harus menjadi baris pertama file.
- **#EXTENC:** - Enkode teks. Itu harus baris ke-2 dari file.
- **#EXTINF:** - Digunakan untuk informasi trek dan properti tambahan lainnya.
- **#PLAYLIST:** - Judul playlist
- **#EXTGRP:** - Mulai pengelompokan nama
- **#EXTALB:** - Informasi album
- **#EXTART:** - Artis album
- **#EXTGENRE** - Genre Album
- **#EXTM3A** - Daftar putar file tunggal untuk trek atau bab album.
- **#EXTBYT:** - Ukuran file dalam byte.
- **#EXTBIN:** - Data biner mengikuti.
- **#EXTIMG:** - Logo, Sampul, atau gambar lainnya.

### HLS M3U ###

HLS (HTTP Live Streaming) dibuat oleh Apple untuk mengalirkan audio dan radio ke perangkat iOS. Ini didasarkan pada M3U diperpanjang yang disandikan UTF-8. Itu distandarisasi sebagai RFC 8216 pada tahun 2017 oleh IETF. Tag untuk playlist HLS dimulai dengan "#EXT-X-". Diberikan di bawah ini adalah daftar tag untuk HLS

- **EXT-X-VERSION** - Menunjukkan versi kompatibilitas file berdasarkan media dan servernya.
- **#EXT-X-START:** - Menunjukkan titik awal yang diinginkan untuk daftar putar.
- **#EXT-X-PLAYLIST-TYPE:** - Menyediakan jenis playlist (EVENT atau VOD).
- **#EXT-X-TARGETDURATION:** - Menentukan durasi Segmen maksimum.
- **#EXT-X-MEDIA-SEQUENCE:** - Menunjukkan Nomor Urutan Media.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Ini menunjukkan bahwa semua sampel media bersifat independen dan dapat didekodekan tanpa segmen lain.
- **#EXT-X-MEDIA:** - Ini digunakan untuk menghubungkan Daftar Putar Media yang berisi Rendisi alternatif dari konten yang sama.
- **#EXT-X-STREAM-INF:** - Menentukan Aliran Varian yang merupakan bagian dari Rendisi.
- **#EXT-X-BYTERANGE:** - Menunjukkan bahwa Segmen Media adalah subrentang sumber daya yang diidentifikasi oleh URI-nya.
- **#EXT-X-DISCONTINUITY** - Menunjukkan diskontinuitas antara segmen media sebelum dan sesudahnya.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Ini memungkinkan sinkronisasi antara rendisi berbeda dari Aliran Varian yang sama atau Aliran Varian yang berbeda.
- **#EXT-X-KEY:** - Menentukan cara mendekripsi Segmen Media.
- **#EXT-X-MAP:** - Menentukan cara mendapatkan Bagian Inisialisasi Media. Diperlukan untuk mengurai Segmen Media yang berlaku.
- **#EXT-X-PROGRAM-DATE-TIME:** - Menghubungkan sampel pertama Segmen Media dengan tanggal dan/atau waktu absolut.
- **#EXT-X-DATERANGE:** - Menghubungkan Rentang Data.
- **#EXT-XI-FRAMES-ONLY** - Mengindikasikan bahwa setiap Segmen Media dalam Daftar Putar mendeskripsikan satu bingkai-I.
- **EXT-XI-FRAME-STREAM-INF** - Ini menunjukkan bahwa file playlist berisi I-frame presentasi Multimedia.
- **#EXT-X-SESSION-DATA:** - Ini memungkinkan data sesi sewenang-wenang
dibawa dalam Daftar Putar Utama.
- **#EXT-X-SESSION-KEY:** - Ini memungkinkan kunci enkripsi. Klien dapat melakukan pramuat kunci ini tanpa membaca daftar putar terlebih dahulu.
- **#EXT-X-ENDLIST** - Ini menunjukkan bahwa tidak ada lagi Segmen Media yang akan ditambahkan ke file.

Berikut ini adalah daftar jenis media Internet yang digunakan oleh M3U:

- **application/vnd.apple.mpegurl**: Ini adalah satu-satunya jenis media terdaftar (terdaftar pada tahun 2009) untuk M3U yang digunakan untuk merujuk ke daftar putar di aplikasi HLS.
- Jenis media Internet berikut digunakan oleh aplikasi non-HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Contoh M3U ##

Ini adalah contoh file M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referensi ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Siaran Langsung HTTP](https://tools.ietf.org/html/rfc8216)

