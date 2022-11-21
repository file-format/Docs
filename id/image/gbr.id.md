{
  "date" : "2019-10-11",
  "keywords" :[ "file gbr", "format file gbr", "apa itu file gbr", "file", "contoh gbr", "ekstensi file gbr", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File GBR - Format File Gerber untuk PCB",
  "description":"Pelajari tentang format file GBR dan API yang dapat membuat dan membuka file GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GBR?

File dengan ekstensi .gbr adalah format file gambar Gerber untuk pertukaran transfer data desain papan sirkuit tercetak (PCB). Ini dikembangkan oleh Ucamco. Data desain PCB adalah komponen utama yang dibutuhkan oleh industri fabrikasi untuk penanganannya. File GRB berisi data PCB seperti lapisan tembaga, topeng solder, legenda, dan data bor dan rute. Ini dapat digunakan untuk mentransfer data seperti karakteristik fabrikasi PCB termasuk ketebalan atau hasil akhir dalam format standar. Semua sistem desain PCB mengeluarkan file Gerber yang dapat ditangani oleh sistem fabrikasi PCB. File GBR kini telah menjadi standar de facto untuk transfer data desain papan sirkuit tercetak (PCB). Ucamco telah menyediakan [penampil online gratis](https://gerber-viewer.ucamco.com/) untuk membuka dan melihat format file GBR.

## Format File GBR

GBR adalah format UTF-8 yang dapat dibaca manusia yang hanya terdiri dari 27 perintah. Karena daftar perintah yang pendek ini dan kekompakannya, GBR mudah untuk di-debug. Gerber pada intinya adalah format vektor terbuka untuk gambar biner 2D. Meta-informasi ditransfer dengan gambar melalui Atribut. Satu file GRB menentukan satu gambar dan tidak memerlukan file yang menyertainya atau parameter eksternal untuk ditafsirkan. Satu gambar hanya membutuhkan satu file. Ini menggunakan karakter ASCII 7-bit untuk semua perintah dan nama yang ditentukan dalam spesifikasi yang dapat dicetak. Ini sepenuhnya mencakup pembuatan gambar lengkap.

### Contoh File GBR

Berikut adalah contoh file Gerber yang membuat lingkaran berdiameter 1,5 mm yang berpusat di titik asal. Ada satu perintah per baris.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referensi

* [Format Gerber](https://www.ucamco.com/en/gerber)

