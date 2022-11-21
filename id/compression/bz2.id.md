{
  "date" : "2019-10-11",
  "keywords" :[ "file bz2", "format file bz2", "apa itu file bz2", "file", "contoh bz2", "ekstensi file bz2", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Format Berkas Terkompresi",
  "description":"Pelajari untuk mengetahui apa itu file BZ2 dan API yang dapat membuat dan membuka file BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Apa itu berkas BZ2?

BZ2 adalah file terkompresi yang dihasilkan menggunakan metode kompresi sumber terbuka [BZIP2](http://www.bzip.org/), kebanyakan pada sistem UNIX atau Linux. Ini digunakan untuk kompresi satu file dan tidak dimaksudkan untuk pengarsipan banyak file. Ini berbeda dengan format file TAR pada platform yang sama yang mengarsipkan banyak file ke dalam satu file tetapi tanpa kompresi. File yang dikompresi sebagai BZ2 dapat didekompresi dengan aplikasi seperti [WinZip](https://www.winzip.com/win/en/). BZIP2 menggunakan algoritma kompresi Run-Length Encoding (RLE) atau [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) untuk mencapai tingkat kompresi yang tinggi.

## Format File BZ2

Tidak ada spesifikasi formal yang tersedia untuk format file ini. Namun, [spesifikasi rekayasa terbalik] tidak resmi (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) menunjukkan bahwa aliran .bz2 terdiri dari header 4 byte yang diikuti dengan nol atau lebih blok terkompresi. Ini segera diikuti oleh penanda end-of-stream yang berisi CRC 32-bit untuk seluruh aliran teks biasa yang diproses. Tidak ada padding antara blok terkompresi dan semua blok diratakan bit.

## Buka zip/Ekstrak File BZ2

Anda dapat mengekstrak file BZ2 di Windows dan Mac OS menggunakan perangkat lunak seperti WinZip. Di linux, perintah berikut di terminal.

```
bzip2 -d filename.bz2
```

## Referensi

* [Spesifikasi Format BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

