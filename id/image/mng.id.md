{
  "date" : "2019-10-11",
  "keywords" :[ "file mng", "format file mng", "apa itu file mng", "file", "contoh mng", "ekstensi file mng", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MNG - Format File Grafik Jaringan Gambar Ganda",
  "description":"Pelajari tentang format file MNG dan API yang dapat membuat dan membuka file MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file MNG?

File dengan ekstensi .mng adalah format file Network Graphics Mutliple-image yang mirip dengan format gambar [PNG](/id/image/png/) tetapi mendukung gambar animasi. Itu dikembangkan untuk menghindari kelebihan format PNG dengan fitur tambahan animasi. MNG juga mirip dengan file [GIF](/id/image/gif/) tetapi menggunakan lebih banyak kompresi dan mendukung fitur alfa penuh. Jenis media MIME tidak resmi untuk file MNG adalah video/x-mng. File MNG dapat dibuka di aplikasi seperti ImageMagik dan IrfanView.

## Format File MNG

Format file MNG mirip dengan PNG dan menggunakan struktur potongan yang sama seperti yang didefinisikan dalam spesifikasi PNG. Dekoder MNG harus dapat mendekode aliran data PNG tanpa menentukan tanda khusus apa pun untuk instruksi dekode. MNG mengelompokkan banyak gambar menjadi satu "bingkai", dengan beberapa gambar digunakan sebagai sprite untuk berpindah dari satu lokasi ke lokasi lain. Mekanisme ini memungkinkan penggunaan kembali data gambar tanpa mentransmisikannya kembali. [Spesifikasi MNG](http://www.libpng.org/pub/mng/spec/) dapat dirujuk untuk referensi pengembang.

### Tanda Tangan MNG

Aliran data MNG dimulai dengan tanda tangan 8-byte yang berisi:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Ini mirip dengan tanda tangan PNG tetapi berisi MNG, bukan PNG.

### Bingkai MNG

Bingkai MNG terdiri dari gambar dua dimensi dari gambar yang lebih kecil. Setiap gambar kecil dapat diakses menggunakan kombinasi indeks baris dan kolom. Format tersebut mampu menyimpan data "voxel" tiga dimensi yang tersusun dalam rangkaian bidang dua dimensi. Setiap pesawat diwakili oleh aliran data PNG atau Delta-PNG. Setiap aliran data Delta-PNG mendefinisikan gambar sebagai perbedaan dari gambar PNG induk. Ini memberikan cara yang jauh lebih ringkas untuk merepresentasikan gambar berikutnya daripada menggunakan aliran data PNG lengkap untuk masing-masing gambar.

## Referensi ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Format MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

