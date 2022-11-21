{
  "date" : "2021-04-08",
  "keywords" :[ "file pkg", "format file pkg", "apa itu file pkg", "file", "contoh pkg", "ekstensi file pkg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Format File Arsip yang Dapat Diperluas",
  "description":"Pelajari tentang format file PKG dan API yang dapat membuat dan membuka file PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Apa itu file PKG?

File dengan ekstensi .pkg adalah file paket penginstal yang digunakan untuk menginstal perangkat lunak di macOS. Selain komputer Macintosh, ini juga digunakan di iPhone. Aplikasi penginstal bawaan Apple dapat digunakan untuk menginstal konten file PKG. File PKG mirip dengan file MSI yang digunakan pada Sistem Operasi Windows untuk instalasi perangkat lunak. Selama instalasi, file-file paket ini dapat mencatat pesan-pesan yang memberi Anda gambaran tentang hal-hal ekstra apa yang diinstal oleh paket ini.

## Format File PKG

PKR adalah file biner yang dikompresi untuk mengurangi ukuran file secara keseluruhan. Sejak OSX 10.5, paket datar dengan file penginstal tunggal telah diperkenalkan oleh Apple. Ini berbeda dari format pengemasan sebelumnya yang datang sebagai bundel daripada file tunggal. Paket yang dibundel ini berisi hierarki direktori terstruktur yang menyimpan file dengan cara yang memfasilitasi pengambilannya melalui beberapa file indeks. Format file PKG datar sebenarnya adalah arsip [XAR](/id/compression/xar/) yang memiliki:

* Header - Mendefinisikan ukuran, checksum, dan informasi versi
* Daftar Isi - Dokumen XML yang (dan harus) dikodekan sebagai UTF-8 dan disimpan di awal file, membuatnya mudah untuk memindai melalui arsip untuk mengekstrak file individual
* Heap - tumpukan data tidak terstruktur yang direferensikan oleh TOC

## Referensi

* [Format File Paket Datar](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

