{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDM - File Bahasa Markup Perangkat Genggam",
  "description":"Pelajari tentang format file HDM dan API yang dapat membuat dan membuka file HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Apa itu file HDM?

File HDM adalah file halaman web bahasa markup yang dibuat dalam Bahasa Markup Perangkat Genggam (HDML). Ini berisi tag markup yang mirip dengan bahasa [HTML](/id/web/html/), tetapi dirancang untuk perangkat elektronik genggam seperti smartphone dan PDA. [Spesifikasi format file HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) dikirim ke W3C untuk standardisasi tetapi tidak dapat menjadi standar. HDM didasarkan pada spesifikasi format file [HDML](/id/web/hdml/) yang tersedia di situs web W3.

## Format File HDM - Informasi Lebih Lanjut

File HDM terdiri dari tag markup yang diberikan ke situs web yang dirancang secara visual pada perangkat genggam. File HDM disalin ke perangkat menggunakan protokol HDTP (Handheld Device Transport Protocol) alih-alih protokol HTTP yang digunakan untuk halaman HTML.

## Elemen Berkas HDML

Berikut ini adalah beberapa elemen yang menyediakan lingkungan run-time untuk HDML dan disebut sebagai agen pengguna.

|Elemen|Deskripsi|
---|---|
|Kartu|Ini adalah blok bangunan dasar HDML, dan menampilkan dan memungkinkan pengguna untuk berinteraksi dengan kartu informasi. |
|Decks|Kartu HDML dikelompokkan bersama ke dalam deck. Dek HDML mirip dengan halaman HTML yang diidentifikasi oleh URL [RFC1738] dan merupakan unit konten yang diminta dari server dan di-cache oleh agen pengguna.|
|Tindakan|Tindakan dapat bertipe PREV, SOFT1-SOFT8, dan HELP. Ini abstrak dan didukung dalam antarmuka pengguna dengan cara khusus agen pengguna.|
|Aktivitas|Aktivitas seperti sekelompok kartu terkait yang melakukan satu fungsi logis. Ini dapat menjangkau satu atau lebih deck. Navigasi HDML dan model status disusun berdasarkan aktivitas.|
|Navigasi berbasis riwayat|Agen pengguna menyimpan riwayat kartu yang ditampilkan kepada pengguna. Setiap kartu yang diakses ditambahkan ke riwayat kartu. Agen pengguna memungkinkan pengguna untuk dengan mudah menavigasi kembali ke kartu sebelumnya dalam riwayat.|

## Referensi

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Spesifikasi HDML - Sekolah W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

