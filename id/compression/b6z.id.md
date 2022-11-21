{
  "date" : "2019-10-11",
  "keywords" :[ "file b6z", "format file b6z", "apa itu file b6z", "file", "contoh b6z", "ekstensi file b6z", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - Format File Arsip B6ZIP",
  "description":"Pelajari tentang format file B6Z dan API yang dapat membuat dan membuka file B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Apa itu file B6Z?

File dengan ekstensi .b6z adalah file arsip terkompresi yang dibuat oleh aplikasi perangkat lunak macOS [B6Zip](http://b6zip.com) yang digunakan untuk mengompres dan mendekompresi file. Ini adalah format arsip yang relatif baru yang memungkinkan rasio kompresi yang lebih tinggi. B6Z memiliki arsitektur terbuka dan mendukung ukuran file hingga 900000 PB. Ini mendukung kompresi data, pemulihan kesalahan, dan rentang file. Perangkat lunak utilitas B6Zip tersedia secara gratis di MacOS untuk membuka berbagai jenis file terkompresi termasuk B6Z.

## Format File B6Z

Format file B6Z didasarkan pada arsitektur terbuka dan memberikan kompresi yang solid dengan algoritme enkripsi AES-256. Ini menggunakan LZMA2 sebagai metode kompresi default, tetapi juga mendukung metode kompresi lainnya sebagai berikut.

|Metode|Deskripsi|
---|---|
|LZMA |Algoritme LZ77 versi optimal|
|LZMA2| Versi LZMA yang ditingkatkan|
|Kempis| Algoritma LZ77 biasa|
|BZip2| Algoritma BWT standar|
|PPMD| PPMdH|Dmitry Shkarin

Utilitas B6Zip mendukung semua standar kompresi ini dan sangat dioptimalkan sehingga menghasilkan kecepatan tinggi. Ini mendukung bekerja dengan format file [ZIP](/id/compression/zip/), [TAR](/id/compression/tar/) dan [RAR](/id/compression/rar/). File B6Z memiliki aplikasi tipe MIME/x-b6z-compressed.

## Referensi

* [B6Zip](http://b6zip.com)

