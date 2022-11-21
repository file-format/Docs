{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File Bahasa Markup Perangkat Genggam",
  "description":"Pelajari tentang format file HDML dan API yang dapat membuat dan membuka file HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Apa itu file HDML?

File dengan ekstensi .hdml (Handheld Device Markup Language) adalah bahasa markup untuk membuat halaman web untuk perangkat elektronik portabel seperti komputer genggam, telepon pintar, dan peralatan tampilan informasi. HDML dikatakan sebagai perpanjangan dari bahasa [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML mirip dengan HTML tetapi untuk perangkat nirkabel dan genggam yang memiliki tampilan kecil seperti PDA, ponsel, dan sebagainya. Itu diganti dengan WML yang bertindak sebagai pengaruh penting.

## Format File HDML - Informasi Lebih Lanjut

HDML adalah bahasa markup untuk perangkat genggam yang didasarkan pada tag markup yang mirip dengan HTML. HDML diserahkan ke W3C untuk standarisasi tetapi tidak pernah menjadi standar. Namun, spesifikasi format filenya tersedia di [situs web W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) untuk referensi. [Sintaksis untuk bahasa HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) tersedia untuk referensi pengembang dan dapat digunakan untuk contoh pengembangan aplikasi.

## Elemen HDML

Berikut ini adalah beberapa elemen yang menyediakan lingkungan run-time untuk HDML dan disebut sebagai agen pengguna.

|Elemen|Deskripsi|
---|---|
|Kartu|Ini adalah blok penyusun dasar HDML, dan menampilkan serta memungkinkan pengguna untuk berinteraksi dengan kartu informasi. |
|Decks|Kartu HDML dikelompokkan bersama ke dalam deck. Dek HDML mirip dengan halaman HTML yang diidentifikasi oleh URL [RFC1738] dan merupakan unit konten yang diminta dari server dan di-cache oleh agen pengguna.|
|Tindakan|Tindakan dapat bertipe PREV, SOFT1-SOFT8, dan HELP. Ini abstrak dan didukung dalam antarmuka pengguna dengan cara khusus agen pengguna.|
|Aktivitas|Aktivitas seperti sekelompok kartu terkait yang melakukan satu fungsi logis. Ini dapat menjangkau satu atau lebih deck. Navigasi HDML dan model status disusun berdasarkan aktivitas.|
|Navigasi berbasis riwayat|Agen pengguna menyimpan riwayat kartu yang ditampilkan kepada pengguna. Setiap kartu yang diakses ditambahkan ke riwayat kartu. Agen pengguna memungkinkan pengguna untuk dengan mudah menavigasi kembali ke kartu sebelumnya dalam riwayat.|

## Referensi

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Spesifikasi HDML - Sekolah W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

