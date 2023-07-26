---
date: 2020-11-11
keywords: myi, .myi, format file myi, cara membuka file myi, ekstensi .myi, ekstensi myi
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File MYI
linktitle: MYI
description: "Pelajari tentang format file MYI dan API yang dapat membuat dan membuka file MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Apa itu File MYI? ##

MYI juga dikenal sebagai file Indeks MySQL MyISAM. Ini digunakan untuk menyimpan indeks untuk tabel MyISAM oleh MySQL. Indeks database MySQL mendefinisikan struktur tabel dan berisi mekanisme kontrol untuk memeriksa integritas tabel.

## Format File MYI ##

File MYI memiliki dua bagian, header, dan nilai kunci.

### Judul MYI ###

Header berisi informasi tentang opsi, ukuran file, dan kunci. Kunci di MySQL dibuat dengan perintah seperti

```sql
CREATE [UNIQUE] INDEX.
```

File yang membaca dan menulis file MYI ada di direktori ./myisam. Ini memiliki file-file berikut:

- mi_open.c: File ini berisi rutin yang menulis setiap bagian dari header.
- mi_create.c: File ini memiliki rutin yang memanggil rutinitas mi_open.c.
- myisamdef.h: File ini memiliki definisi struktur.

Header memiliki bagian berikut:

- status: Status ditulis oleh mi_open.c, mi_state_info_write(). Struktur ini terjadi sekali dalam file.
- basis: Basis ditulis oleh mi_open.c, mi_base_info_write(). MI_BASE_INFO adalah struktur yang sesuai untuk basis di myisamdef.h. Struktur ini terjadi sekali dalam file.
- keydef: Keydef ditulis oleh mi_open.c, mi_keydef_write(). MI_KEYDEF adalah struktur yang sesuai untuk keydef di myisamdef.h. Ini adalah struktur kejadian ganda yang muncul untuk setiap indeks.
- recinfo: Recinfo ditulis oleh mi_open.c, mi_recinfo_write(). MI_COLUMNDEF adalah struktur yang sesuai untuk recinfo di myisamdef.h. Ini adalah struktur kejadian ganda yang muncul satu kali dari setiap bidang yang muncul di kunci.

### Nilai Kunci ###

Halaman di MySQL disebut blok. Nilai kunci ada di blok. Sebuah blok berisi informasi hanya dari satu indeks. Setiap kunci berisi seluruh isi dari semua kolom. Panjang blok normal adalah 0x0400 (1024) byte. Penunjuk memiliki nomor ukuran tetap (4-byte) untuk tabel baris tetap yang berisi nomor baris ordinal. Jika kuncinya null maka bytenya adalah 0x00. Blok normal setidaknya 65% penuh dan biasanya 80% penuh.

File myisamdef.h berisi informasi berikut yang dinyatakan dalam konstanta. Jumlah maksimal kunci adalah 32 (MI_MAX_KEY) dan jumlah maksimal segmen dalam sebuah kunci adalah 16 (MI_MAX_KEY_SEG). Panjang maksimum kunci adalah 500 (MI_MAX_KEY_LENGTH). Panjang maksimum blok adalah 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referensi ##

- [File .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

