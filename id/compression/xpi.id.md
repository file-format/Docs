{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - File Paket Penginstal Lintas Platform",
  "description":"Pelajari tentang format file XPI dan API yang dapat membuat dan membuka file XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Apa itu file XPI?

File XPI adalah arsip instalasi yang dikompresi untuk mengurangi ukuran file. Ini digunakan oleh aplikasi Mozilla untuk instalasi plugin dan file add-on. Ini berisi skrip instalasi atau manifes di root file bersama dengan sejumlah file data. File XPI mungkin berisi tema, toolkit, atau plugin Firefox yang dapat diinstal pengguna untuk menjadi bagian dari browser Firefox, Thunderbird, atau SeaMonkey.

## Format File XPI - Informasi Lebih Lanjut

File XPI disimpan ke disk sebagai arsip [ZIP](/id/compression/zip/) yang menggabungkan beberapa file menjadi satu file terkompresi. File di dalam file XPI dapat menyertakan file skrip penginstalan seperti JS dan file web seperti [CSS](/id/web/css/), [HTML](/id/web/html/) dan [JSON](/id/web/json/ ). Kadang-kadang, mungkin juga berisi file gambar [PNG](/id/image/png/) untuk digunakan sebagai ikon oleh add-on.

### Bagaimana cara melihat konten file XPI?

File XPI praktis adalah arsip ZIP yang isinya dapat dilihat menggunakan langkah-langkah berikut.

* Ubah ekstensi file dari XPI ke ZIP
* Ekstrak konten file menggunakan utilitas dekompresi standar seperti WinZip (Windows, Mac), 7-Zip (Windows), atau Apple Archive Utility (Mac).

### Instal File XPI di Firefox Android

Kebanyakan orang ingin tahu apakah file XPI dapat diinstal di Firefox pada perangkat Android. Di Android, Anda dapat menginstal add-on dari file XPI dengan mencari file tersebut dan membukanya dengan Firefox.

## Referensi

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Bagaimana cara membuka Ekstensi File XPI?](https://support.mozilla.org/en-US/questions/1009049)

