---
date: 2020-08-12
keywords: flif, .flif, format file flif, cara membuka file flif, ekstensi .flif, ekstensi flif
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File FLIF
linktitle: FLIF
description: "Pelajari tentang format file FLIF dan API yang dapat membuat dan membuka file FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Apa itu file FLIF? ##

FLIF (Free Lossless Image Format) adalah format gambar lossless yang menggunakan ekstensi .flif untuk filenya. FLIF mengklaim mengungguli [PNG](/id/image/png/), lossless [WebP](/id/image/webp/), lossless BPG, dan lossless JPEG 2000 dalam hal rasio kompresi. FLIF menggunakan interlacing progresif, sehingga setiap unduhan sebagian gambar dapat digunakan sebagai penyandian lossy untuk seluruh gambar.

## Sejarah Singkat ##

FLIF diumumkan pada September 2015, dan versi alfa dirilis pada Oktober 2015. Pada September 2016, versi stabil pertama dari FLIF dirilis.

## Desain FLIF ##

FLIF menggunakan varian CABAC (pengkodean aritmatika biner konteks-adaptif), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) untuk kompresi. MANIAC adalah algoritma pengkodean entropi yang dikembangkan oleh Jon Sneyers dan Pieter Wuille. Dalam MANIAC, konteksnya adalah node pohon keputusan yang dipelajari pada waktu pengkodean secara dinamis. Ini membuat model konteks lebih spesifik untuk gambar dan menghasilkan kompresi yang lebih baik. FLIF memiliki beberapa fitur berikut:

- Mendukung kompresi lossless
- Mendukung kompresi lossy dengan preprocessing encoder
- Mendukung Skala Abu-abu, RGB, dan RGBA
- Mendukung kedalaman warna 1 hingga 16 bit per saluran
- Mendukung file interlaced dan non-interlaced
- Mendukung decoding progresif dari file yang diunduh sebagian
- Mendukung animasi
- Mendukung profil warna ICC tersemat, metadata Exif dan XMP
- Memiliki dukungan terbatas untuk mengompresi file mentah kamera (RGGB)

## Format File FLIF ##

File FLIF memiliki empat bagian berikut:

## Tajuk Utama ##

Header utama berisi metadata utama termasuk lebar, tinggi, kedalaman warna, jumlah bingkai.

|Jenis|Nilai|Deskripsi|
|---|---|---|
|4 byte|"FLIF"|Sihir|
|4 bit|3 = ni diam; 4 = saya masih; 5 = ni anim; 6 = i anim|Interlacing, animasi|
|4 bit|1 = Skala abu-abu; 3 = RGB; 4 = RGBA|Jumlah saluran (nb_channels)|
|1 byte|'0','1','2' ('0'=khusus)|Byte per saluran (Bpc)|
|varian|lebar-1|Lebar|
|varint|tinggi-1|Tinggi|
|varint|nb_frames-2 (hanya jika animasi)|Jumlah frame (nb_frames)|

## Potongan metadata ##

Bagian ini berisi non-piksel seperti metadata Exif/XMP, profil warna ICC, dll. yang dikodekan menggunakan kompresi DEFLATE. Potongan ini didefinisikan mirip dengan potongan PNG dengan perbedaan bahwa ukuran chuck dikodekan dengan sejumlah variabel byte. Nama bongkahan dapat berupa 4 huruf (4 byte) atau nilai di bawah 32 yang menunjukkan bongkahan non-opsional.

Berikut ini adalah contoh chuck opsional:

|Nama bongkahan|Deskripsi|Konten (setelah dekompresi DEFLATE)|
|---|---|---|
|iCCP|profil warna ICC|data profil warna ICC mentah|
|eXif|Exif metadata|"Exif\0\0" header diikuti oleh TIFF header dan data EXIF|
|eXmp|metadata XMP|XMP terkandung dalam xpacket read-only tanpa padding|

### Konvensi penamaan ###

- **Huruf Pertama**: Huruf besar digunakan untuk bagian penting dan huruf kecil digunakan untuk bagian yang tidak penting.
- **Huruf Kedua**: Huruf besar digunakan untuk umum dan huruf kecil digunakan untuk potongan pribadi
- **Huruf Ketiga**: Huruf besar digunakan untuk chuck yang diperlukan untuk menampilkan gambar dengan benar dan huruf kecil tidak penting untuk menampilkan gambar.
- **Huruf Keempat**: Huruf besar digunakan untuk chuck yang dapat disalin dengan aman secara membabi buta. Chuck huruf kecil bergantung pada data gambar.

## Tajuk Kedua ##

Ini berisi informasi mengenai penyandian sebenarnya dari piksel.

|Tipe|Deskripsi|Kondisi|Nilai Default|
|---|---|---|---|
|1 byte|NUL byte (0x00), nama potongan dari bitstream FLIF16||
|uni_int(1,16)|Bits per piksel saluran|Bpc == '0': ulangi(nb_channels)|8 jika Bpc == '1', 16 jika Bpc == '2'|
|uni_int(0,1)|Bendera: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Jumlah loop|nb_frame > 1||
|uni_int(0,60_000)|Penundaan bingkai dalam ms|nb_frames > 1: ulangi(nb_frames)|
|uni_int(0,1)|Bendera: has_custom_cutoff_and_alpha|||
|uni_int(1.128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|pembagi alfa|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Tandai: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variabel|Transformasi (lihat di bawah)|||
|uni_int(1) = 0|Bit indikator: selesai dengan transformasi|||
|uni_int(0,2)|Prediktor piksel tak terlihat|alpha_zero && interlaced && rentang alpha termasuk nol||

**Saluran**

|Nomor saluran|Deskripsi|
|---|----|
|0|Merah atau Abu-abu|
|1|Hijau|
|2|Biru|
|3|Alfa|

**Transformasi**

|Jenis|Deskripsi|
|---|---|
|uni_int(1) = 1|Bit indikator: belum selesai|
|uni_int(0,13)|Pengidentifikasi transformasi|
|variabel|Transformasi data (tergantung pada transformasi)|

Transformasi digunakan untuk memodifikasi data piksel untuk kompresi yang lebih baik dan untuk melacak nilai piksel yang sebenarnya terjadi.

## Data Piksel ##

Bagian ini berisi data piksel aktual yang dikodekan menggunakan pengkodean entropi MANIAC. Piksel dapat dikodekan menggunakan pengkodean interlaced atau non-interlaced.

### Metode interlaced ###

Dalam metode ini, tingkat zoom ditentukan. Zoomlevel 0 digunakan untuk gambar penuh, zoomlevel 1 digunakan untuk semua baris bernomor genap, zoomlevel 2 digunakan untuk semua kolom genap dari zoomlevel 1. Dengan kata lain, setiap zoomlevel 2k bernomor genap adalah versi downsampled dari gambar, pada skala 1:2^k. Zoomlevels dikodekan dari tertinggi ke terendah.

### Metode non-interlaced ###

Dalam metode ini, pengkodean pohon MANIAC dimulai segera diikuti dengan pengkodean piksel.

## Referensi ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

