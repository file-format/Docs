{
  "date" : "2021-04-08",
  "keywords" :[ "file rpm", "format file rpm", "apa itu file rpm", "file", "contoh rpm", "ekstensi file rpm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - File Manajer Paket Red Hat",
  "description":"Pelajari tentang format file RPM dan API yang dapat membuat dan membuka file RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Apa itu file RPM?

File dengan ekstensi .rpm adalah paket sistem operasi Red Hat Linux untuk instalasi program di sistem Linux. Red Hat Package Manager menggunakan format file RPM dan merupakan sistem manajemen paket sumber terbuka dan gratis. Meskipun file RPM dapat digunakan untuk instalasi program, ini dapat dikonversi ke format paket lain seperti [DEB](/id/compression/deb/) menggunakan program Debian yang disebut Alien.

## Format File RPM

File RPM adalah biner yang dapat berisi sekumpulan file. Sering kali, file RPM adalah "RPM biner" yang merupakan kompilasi perangkat lunak yang dapat dieksekusi. File RPM dapat berisi RPM sumber (SRPM) yang dapat digunakan untuk membangun paket dari kode sumber. Format file RPM terdiri dari empat bagian.

* Timbal - Ini mengidentifikasi file sebagai file RPM
* Tanda Tangan - Dapat digunakan untuk memastikan integritas dan/atau keaslian
* Header - Berisi metadata termasuk nama paket, versi, arsitektur, daftar file, dll.
* Arsip File - Juga dikenal sebagai payload, yang biasanya dalam format cpio, dikompresi dengan [GZIP](/id/compression/gz/)

## Referensi

* [RPM - Wikipedia](https://rpm.org)
* [Dokumentasi RPM](https://rpm.org/documentation.html)

