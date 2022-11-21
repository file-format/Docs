---
date: 2019-10-11
keywords: langkah, .langkah, format file langkah, cara membuka file langkah, ekstensi .langkah, ekstensi langkah
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File LANGKAH
linktitle: STEP
description: "Pelajari tentang format file STEP dan API yang dapat membuat dan membuka file STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Apa itu file LANGKAH?

File STEP adalah format pertukaran data yang banyak digunakan untuk Computer-aided design (CAD). Itu distandarisasi pada tahun 1994 oleh komite ISO dengan nama "ISO 10303-21". ISO 10303-21 mendefinisikan mekanisme pengkodean untuk merepresentasikan data dalam bahasa pemodelan data EXPRESS. File LANGKAH- juga dikenal sebagai File-p21 dan File Fisik LANGKAH. Ekstensi file yang digunakan untuk file STEP adalah .stp dan .step.

## Sejarah Dasar

Pada tahun 1994, spesifikasi Bagian 21 asli dikeluarkan. Ini memiliki beberapa bug yang diperbaiki oleh corrigendum teknis yang dikeluarkan pada tahun 1996. Edisi kedua diterbitkan pada tahun 2002 yang mencakup corrigendum dan ekstensi untuk beberapa bagian data. Edisi ketiga diterbitkan pada tahun 2016 yang menambahkan bagian jangkar dan referensi yang memungkinkan entitas dan nilai disimpan dalam file eksternal. Dukungan UTF-8 ditambahkan string. Tanda tangan digital ditambahkan untuk memverifikasi isi file dan untuk memvalidasi kredensial. Dukungan untuk mengompresi dan menyimpan struktur pertukaran menggunakan ZIP juga ditambahkan.

## Format File LANGKAH

Format teks biasa untuk file STEP terdiri dari urutan catatan. Kumpulan karakter didefinisikan sebagai poin kode ISO 10646. "ISO-10303-21;" adalah karakter pertama dalam rekaman pertama. Komentar dikelilingi oleh karakter "/*" dan "*/". Rekaman terakhir berisi "END-ISO-10303-21;" jika file LANGKAH sesuai dengan versi 2002. Jika sesuai dengan versi 2016, mungkin ada satu atau lebih tanda tangan digital setelah "END-ISO-10303-21;" terminator. Hentian baris dilambangkan dengan "\N\" dan jeda halaman dilambangkan dengan "\F\".

File STEP dibagi menjadi beberapa bagian dan namanya adalah istilah yang dicadangkan. Semua bagian diakhiri dengan catatan "ENDSEC" dan harus dalam urutan yang ditunjukkan di bawah ini.

- **HEADER**: Ini adalah bagian wajib dan tidak dapat diulang. Ini terdiri dari entitas berikut:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Ini adalah bagian opsional yang tidak berulang yang diperkenalkan pada versi 2016. Ini mendefinisikan nama eksternal untuk instance sehingga dapat direferensikan.
- **REFERENSI**: Ini adalah bagian opsional yang tidak berulang yang juga diperkenalkan pada versi 2016. Setiap entri di bagian ini mengaitkan nama instance entri/nilai ke instance/nilai dalam file eksternal.
- **DATA**: Ini adalah bagian berulang opsional yang berisi konten inti dari instance model.
- **SIGNATURE**: Ini adalah bagian berulang opsional yang diperkenalkan pada versi 2016. Itu memegang tanda tangan digital untuk memverifikasi konten file atau untuk memvalidasi kredensial.

## Referensi

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

