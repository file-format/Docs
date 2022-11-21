{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "ekstensi", "file", "format file", "Tipe File Basis Data", "Format File Basis Data", "Basis Data Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file BTR dan API yang dapat membuat dan membuka file BTR.",
  "title" :"BTR - Berkas Basis Data Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Apa itu file BTR?

File dengan ekstensi .btr adalah file database yang dibuat oleh [Btrieve](https://www.actian.com/) aplikasi database transaksional. Tidak seperti sistem manajemen database relasional (RBMS), Btrieve didasarkan pada Indexed Sequential Access Method (ISAM), yang merupakan cara menyimpan data untuk pengambilan cepat. File BTR menyimpan kumpulan catatan dan digunakan untuk menghasilkan laporan sesuai kebutuhan. File BTR dapat dibuka menggunakan Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility, dan Legend Software BTRIEVE Viewer.

## Struktur File BTR - Informasi Lebih Lanjut

Struktur data internal dan penyelarasan setiap byte dalam struktur file BTR tidak tersedia untuk umum. Namun, Btrieve
menyediakan [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) yang dapat digunakan untuk membaca informasi dari file BTR. Ini kompatibel dengan bahasa pemrograman dan lingkungan pengembangan berikut.

* Embarcadero C/C++
*Embarcadero Delphi
* GNU C/C++
* COBOL Fokus Mikro
*Microsoft VisualBasic
*Microsoft Visual C++
* Watcom C/C++

Mengambil data dari file BTR bergantung pada file DDF yang terkait dengannya. Tanpa DDF, tidak akan mudah mengambil informasi dari file semacam itu.

## Referensi

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Pengantar Btreive API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

