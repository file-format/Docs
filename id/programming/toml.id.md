---
date: 2019-10-11
keywords: toml, .toml, format file toml, cara membuka file toml, ekstensi .toml, ekstensi toml
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File TOML
linktitle: TOML
description: "Pelajari tentang format file TOML dan API yang dapat membuat dan membuka file TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Apa itu file TOML? ##

TOML (Tom's Obvious Minimal Language) adalah format file konfigurasi minimal yang menggunakan ekstensi .toml. TOML bertujuan agar mudah dibaca, dipetakan dengan jelas ke kamus, dan mudah diurai ke struktur data yang berbeda. TOML memiliki spesifikasi sumber terbuka yang menerima kontribusi komunitas. TOML didukung oleh banyak bahasa pemrograman seperti C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, dll. Tipe MIME untuk file TOML adalah *application/toml*.


## Format File TOML ##

File TOML terutama terdiri dari Pasangan kunci/nilai, bagian/tabel, komentar, dan harus berupa dokumen Unicode berenkode UTF-8 yang valid. TOML mendukung tipe data String, Integer, Float, Boolean, Datetime, Array, dan Tabel (tabel hash/kamus). TOML adalah bahasa yang peka terhadap huruf besar-kecil.

### Sintaks ###

- **Pasangan Nilai-Kunci**: Pasangan nilai-kunci dipisahkan dengan tanda sama dengan (=). Setiap pasangan harus berada di baris baru.

``` toml
pertama = "Tom"
terakhir = "Preston-Werner"
```

- **Komentar**: Komentar dimulai dengan simbol hash (#).

``` toml
# Ini adalah dokumen TOML.
```

- **String**: String diapit oleh tanda kutip ("").

``` toml
string = "Contoh String"
```

- **String Multi-baris**: String multi-baris diapit oleh tiga tanda kutip (""").

``` toml
[alamat rumah]
jalan = """123 Tornado Alley
Kamar 16"""
kota = "Pusat Tengah Timur"
status = "KS"
```

- **Integer/Float**

``` toml
bilangan bulat = 20
mengambang = 20,5
```

- **Boolean**: Boolean selalu huruf kecil.

``` toml
bool1 = benar
bool2 = salah
```

- **Tanggal-Waktu**: Untuk TanggalWaktu, Anda dapat menggunakan tanggal-waktu berformat RFC 3339 seperti yang ditunjukkan pada contoh di bawah ini.

``` toml
offset_date_time = 27-05-1979 07:32:00 Z
local_date_time = 1979-05-27T07:32:00
tanggal_lokal = 27-05-1979
waktu_lokal = 07:32:00
```

- **Array**: Array diapit oleh tanda kurung siku dengan elemen dipisahkan oleh koma (,).

``` toml
warna = [ "merah", "kuning", "hijau" ]
```

- **Tabel**: Tabel adalah kumpulan pasangan kunci/nilai yang ditentukan oleh header pada baris baru yang diapit tanda kurung siku ([]). Tabel berakhir saat header baru disediakan atau saat file berakhir.

``` toml
[alamat rumah]
jalan = """123 Tornado Alley
Kamar 16"""
kota = "Pusat Tengah Timur"
status = "KS"

[alamat kantor]
jalan = """123 Tornado Alley
Kamar 16"""
kota = "Pusat Tengah Timur"
status = "KS"
```

Tabel sebaris diapit oleh kurung kurawal ({}) dengan setiap pasangan kunci/nilai dipisahkan dengan koma (,).

``` toml
nama = { pertama = "Tom", terakhir = "Pitt" }
```

## Referensi ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

