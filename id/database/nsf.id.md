{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file NSF dan API yang dapat membuat dan membuka file NSF.",
  "title" :"Format File NSF - Format Basis Data Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file NSF?

File dengan ekstensi .nsf (Fasilitas Penyimpanan Notes) adalah format file database yang digunakan oleh [perangkat lunak IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), yang sebelumnya dikenal sebagai Lotus Notes. Ini mendefinisikan skema untuk menyimpan berbagai jenis objek seperti email, janji temu, dokumen, formulir, dan tampilan. Semua informasi ini terkandung dalam satu file NSF untuk kolaborasi bisnis yang serupa dengan file PST/OST. Beberapa aplikasi yang dapat membuka file NSF antara lain IBM Lotus Notes dan IBM Domino.

## Spesifikasi Format File NSF

File NSF bersifat biner dan spesifikasinya tersedia oleh Joachim Metz di [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Sesuai perincian ini, file NSF terdiri dari:

* Judul File
* Kepala Basis Data

Selain itu, terdiri dari:

* Superblok
* Blok deskriptor ember
* Bitmap
* Rekam ember Vektor Relokasi
* Ringkasan ember
* Ember non-ringkasan


### Tajuk Berkas NSF

Header file NSF berukuran 6 byte. Terdiri dari:

|Offset|Ukuran|Nilai|Deskripsi|
---|---|---|---|
0|2|0x1a 0x00|Tanda Tangan|
2|4| |Ukuran tajuk basis data|

### Header basis data

Header NSD Database berisi nilai yang dikonfirmasi berikut ini.

* Informasi Basis Data
* Pengidentifikasi basis data (DBID)
* Informasi replikasi
* Bendera penyangga informasi basis data
* Judul
* Kategori
* Kelas
* Kelas desain (nama templat)
* Pengidentifikasi catatan khusus
* Bantalan
* Informasi basis data 2
* Informasi basis data 3
* Informasi basis data 4
* Basis data informasi 5
* Bantalan
* Pengidentifikasi instance basis data (DBIID)
* Sejarah replikasi

## Referensi

* [Format NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

