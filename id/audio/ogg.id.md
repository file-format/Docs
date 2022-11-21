---
date: 2019-12-13
keywords: ogg, format file ogg, ekstensi .ogg, format audio ogg
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Pelajari tentang format file OGG dan API yang dapat membuat dan membuka file OGG."
title: File OGG - File Audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Apa itu file OGG?

OGG adalah File Audio Terkompresi Ogg Vorbis yang disimpan dengan ekstensi .ogg. File OGG digunakan untuk menyimpan data audio dan dapat menyertakan informasi artis dan trek serta metadata juga. OGG adalah format kontainer gratis dan terbuka yang dikelola oleh Yayasan Xiph.Org.

## Sejarah Singkat Format File OGG

Proyek Ogg dimulai sebagai bagian dari proyek yang lebih besar pada tahun 1993 dan diberi nama Squish tetapi karena merek dagang yang ada, namanya diubah menjadi OggSquish. Itu digambarkan sebagai upaya untuk membuat format audio terkompresi yang fleksibel untuk aplikasi audio modern. Referensi OGG dipisahkan dari Vorbis pada tanggal 2 September 2000.

OGM dibuat pada tahun 2002 karena kurangnya dukungan video formal di OGG. Ini memungkinkan penyematan video dari kerangka kerja Microsoft DirectShow ke dalam pembungkus berbasis OGG. Pada tahun 2006, OGG didukung oleh banyak mesin video game dan biasanya digunakan untuk menyandikan konten gratis. Free Software Foundation memulai kampanye pada 15 Mei 2007, untuk meningkatkan penggunaan Vorbis sebagai alternatif unggul MP3. Pada tanggal 30 Juni 2009, OGG adalah satu-satunya format kontainer yang didukung oleh implementasi HTML5 dari Firefox 3.5.

## Format File OGG

Format OGG terdiri dari potongan data. Setiap potongan disebut halaman Ogg. Setiap halaman dimulai dengan "OggS" untuk mengidentifikasi Format Ogg. Header berisi nomor seri dan nomor halaman yang mengidentifikasi setiap halaman sebagai bagian dari rangkaian. Halaman terdiri dari komponen-komponen berikut.

- **Kepala halaman**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Sedikit | Nilai | Deskripsi |
| --- | --- | --- |
| 0 | 0x01 | Menunjukkan bahwa paket pertama halaman adalah kelanjutan dari paket sebelumnya dalam bitstream logis. |
| 1 | 0x02 | Menunjukkan bahwa halaman ini adalah yang pertama dalam bitstream logis. |
| 2 | 0x04 | Menunjukkan bahwa halaman ini adalah yang terakhir dalam bitstream logis. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadata**: VorbisComment adalah mekanisme yang paling banyak didukung untuk menyimpan metadata. Mekanisme lain termasuk yang berikut:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referensi ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

