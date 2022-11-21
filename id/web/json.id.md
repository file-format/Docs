---
date: 2019-10-11
keywords: json, .json, format file json, cara membuka file json, notasi objek javascript, format data json, format file .json
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File JSON - Apa itu file JSON?
linktitle: JSON
description: "Pelajari tentang format file JSON dan API yang dapat membuat dan membuka file JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Apa itu file JSON?

JSON (JavaScript Object Notation) adalah format file standar terbuka untuk berbagi data yang menggunakan teks yang dapat dibaca manusia untuk menyimpan dan mengirimkan data. File JSON disimpan dengan ekstensi .json. JSON memerlukan lebih sedikit pemformatan dan merupakan alternatif yang baik untuk [XML](/id/web/xml/). JSON berasal dari JavaScript tetapi merupakan format data yang tidak tergantung bahasa. Pembuatan dan penguraian JSON didukung oleh banyak bahasa pemrograman modern. *application/json* adalah jenis media yang digunakan untuk JSON.

## Format File JSON - Sejarah Singkat

Ada kebutuhan untuk komunikasi server waktu nyata ke klien yang mengarah pada pembuatan JSON. Format JSON pertama kali ditentukan oleh Douglas Crockford pada Maret 2001. JSON didasarkan pada Standard ECMA-262 3rd Edition—Desember 1999 yang merupakan bagian dari JavaScript.

Edisi pertama standar JSON ECMA-404 diterbitkan pada Oktober 2013 oleh Ecma International. RFC 7159 menjadi acuan utama penggunaan Internet JSON pada tahun 2014. Pada November 2017, ISO/IEC 21778:2017 diterbitkan sebagai standar internasional. RFC 8259 diterbitkan pada 13 Desember 2017 oleh The Internet Engineering Task Force yang merupakan versi standar Internet STD 90 saat ini.

## Struktur File JSON

Data JSON ditulis dalam pasangan **kunci/nilai**. Kunci dan nilai dipisahkan oleh tanda titik dua (:) di tengah dengan kunci di sebelah kiri dan nilai di sebelah kanan. Pasangan kunci/nilai yang berbeda dipisahkan oleh koma (,). Kuncinya adalah string yang diapit oleh tanda petik ganda misalnya "nama". Nilai dapat dari jenis berikut.

- `Nomor`
- `String`: Urutan karakter Unicode diapit oleh tanda kutip ganda.
- `Boolean`: Benar atau Salah.
- `Array`: Daftar nilai yang diapit tanda kurung siku, misalnya

``` json
[ "Apel", "Pisang", "Jeruk" ]
```

- `Objek`: Kumpulan pasangan kunci/nilai yang dikelilingi oleh kurung kurawal, misalnya

``` json
{"name": "Jack", "age": 30, "favoriteSport" : "Football"}
```

Objek JSON juga dapat disarangkan untuk mewakili struktur data. Diberikan di bawah ini adalah contoh objek JSON.

### Contoh Format JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Berapa ukuran maksimum file JSON?

Praktis tidak ada batasan ukuran maksimum file JSON. Itu bisa selama ruang yang dibutuhkan oleh konten untuk disimpan.

Ketika menggunakan format file JSON untuk mentransfer data melalui internet, seseorang harus berhati-hati dengan sumber daya komputer yang tersedia. Jika data JSON besar ditransfer, transfer akan terpengaruh jika browser klien memiliki memori terbatas.


Tidak ada batasan pasti yang ditentukan oleh spesifikasi, tetapi Anda harus berhati-hati agar tidak menghabiskan sumber daya di komputer pengguna, karena hal itu akan menurunkan pengalaman pengguna dengan cepat, dan kemungkinan besar mereka akan meninggalkan aplikasi Anda.

## JSON vs XML

**XML** adalah format file lain yang umum dan banyak digunakan untuk pertukaran data melalui internet. Dalam hal pertukaran data antar aplikasi, pengembang memiliki opsi untuk menggunakan format file XML dan JSON. Namun, JSON diadopsi sebagai cara paling nyaman untuk pertukaran data antar aplikasi melalui internet karena alasan berikut.

1. JSON memberikan tampilan data yang jelas dan lebih mudah dibaca dibandingkan dengan format file XML
1. JSON mengurangi overhead transfer data melalui internet karena jumlah karakternya lebih sedikit untuk menentukan kumpulan data yang sama dibandingkan dengan XML
1. Bahasa pemrograman modern menyediakan parser bawaan untuk mengurai respons JSON melalui web.

## Tahukah kamu?

Anda dapat menjadi kontributor di FileFormat.com agar komunitas format file tetap up to date dengan temuan Anda. Jika Anda harus membagikan sesuatu tentang JSON atau format file Web, Anda dapat memposting temuan Anda di bagian [Berita Format File Web](https://news.fileformat.com/t/Web) agar orang-orang dapat mempelajari lebih lanjut dari ini.

## Referensi

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Pengantar JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

