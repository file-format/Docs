---
date: 2019-10-11
keywords: WEBM, Apa itu file WEBM, Format File WEBM
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Pelajari tentang format file WEBM dan API yang dapat membuat dan membuka file WEBM."
title: WEBM - Format File Video WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Apa itu file WEBM?

File dengan ekstensi .webm adalah file video berdasarkan format file WebM terbuka dan bebas royalti. Ini telah dirancang untuk berbagi video di web dan menentukan struktur wadah file termasuk format video dan audio. WebM 100% gratis, menerapkan kualitas tinggi berdasarkan teknologi terbuka seperti HTML, HTTP, dan TCP/IP yang terbuka bagi siapa saja untuk implementasi. WebM telah dirancang khusus untuk menyajikan video di web yang membuatnya dioptimalkan untuk streaming dengan jejak komputasi yang rendah. Ini membuatnya cocok untuk pemutaran video di perangkat apa pun terutama netbook, perangkat genggam, dan tablet berdaya rendah.

## Format File WEBM

Struktur file WebM didasarkan pada subset dari format file container Matroska [MKV](/id/video/mkv/). Streaming video yang tersedia dalam file WebM dikompresi menggunakan teknologi kompresi VP8 atau VP9 yang sangat efisien dalam kompresi. Demikian pula, streaming audio dalam file WebM dikompresi menggunakan codec Vorbis atau Opus yang dikembangkan oleh [Xiph Foundation](https://www.xiph.org/). Semua video dan codec audio ini bebas royalti dan dapat digunakan tanpa biaya apa pun.

Berikut adalah ringkasan spesifikasi untuk format file WebM.

|Bidang|Deskripsi|
---|---|
|Jenis MIME |video/webm|
|Jenis MIME khusus audio |audio/webm|
|Pengidentifikasi Jenis Seragam| org.webmproject.webm|
|Nama Kodek Video| VP8 atau VP9|
|Nama Kodek Audio| Vorbis atau Opus|

### Elemen WebM

WebM, sebagai bagian dari spesifikasi Matroska, memberikan dukungan untuk beberapa fungsi Matroska. Berikut ini adalah deskripsi elemen yang didukung.

####EBML

|Nama |Deskripsi|
---|---|
|EBML|Atur karakteristik EBML dari data yang akan diikuti. Setiap dokumen EBML harus dimulai dengan ini.|
|EBMLVersion |Versi parser EBML yang digunakan untuk membuat file.|
|EBMLReadVersion|Versi EBML minimum yang harus didukung parser untuk membaca file ini.|
|EBMLMaxIDLength |Panjang maksimum ID yang akan Anda temukan di file ini (4 atau kurang di Matroska).|
|EBMLaxSizeLength|Panjang maksimum ukuran yang akan Anda temukan di file ini (8 atau kurang di Matroska). Ini tidak mengesampingkan ukuran elemen yang ditunjukkan di awal elemen. Elemen yang memiliki ukuran terindikasi lebih besar dari yang diizinkan oleh EBMLMaxSizeLength akan dianggap tidak valid.|
|DocType|Sebuah string yang mendeskripsikan jenis dokumen yang mengikuti header EBML ini ("webm" dalam kasus kita).|
|DocTypeVersion|Versi juru bahasa DocType yang digunakan untuk membuat file.|
|DocTypeReadVersion|Versi DocType minimum yang harus didukung juru bahasa untuk membaca file ini.|

#### Elemen Global

Saat ini, hanya elemen `Void` yang didukung yang digunakan untuk membatalkan data yang rusak, untuk menghindari perilaku tak terduga saat menggunakan data yang rusak. Konten tersebut dibuang. Juga digunakan untuk memesan ruang di sub-elemen untuk digunakan nanti.

#### Segmen
Elemen ini berisi semua elemen level atas (level 1) lainnya. Biasanya file Matroska terdiri dari 1 segmen.

#### Meta Mencari Informasi

Informasi pencarian berikut ini didukung.

|Nama Elemen |Deskripsi|
---|---|
|SeekHead |Berisi posisi elemen level 1 lainnya.|
|Seek |Berisi entri pencarian tunggal ke elemen EBML.|
|SeekID |ID biner yang sesuai dengan nama elemen.|
|SeekPosition |Posisi elemen dalam segmen dalam oktet (0 = elemen level 1 pertama).|

## Referensi

* [WebM](https://www.webmproject.org/)
* [Repositori Kode WebM](https://www.webmproject.org/code/#webp-repositories)

