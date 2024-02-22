{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File ZST - Format File Terkompresi Zstandar",
  "description":"Pelajari tentang format file ZST dan API yang dapat membuat dan membuka file ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-id",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Apa itu file ZST?

File ZST adalah file terkompresi yang dihasilkan dengan algoritma kompresi Zstandard (zstd). Ini adalah file terkompresi yang dibuat dengan kompresi lossless oleh algoritma. File ZST dapat digunakan untuk mengompresi berbagai jenis file seperti database, sistem file, jaringan, dan game. Zstandard diatur oleh [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) yang menjelaskan keseluruhan mekanisme kompresi, jenis media, dan pengkodean konten.

## Format File ZST

File ZST disimpan dalam format file terkompresi ke disk. Mekanisme kompresi seperti yang dijelaskan oleh RFC 8878 yang menggantikan RFC 8478.

## Bingkai ZST

File ZST terdiri dari satu atau lebih frame. Setiap frame dapat berupa frame Zstandard atau frame yang dapat dilewati. Bingkai Zstandard berisi data terkompresi, sedangkan bingkai yang dapat dilewati berisi metadata pengguna khusus.

### Bingkai Zstandar

Bingkai Zstandard memiliki struktur berikut.

|Bidang|Ukuran dalam Byte|
---|---|
|Nomor_ Ajaib |4 byte|
|Frame_Header |2-14 byte|
|Blok_Data |n byte|
|[Lebih Banyak Data_Blok] ||
|[Content_Checksum] |4 byte|

### Bingkai yang Dapat Dilewati

Bingkai yang dapat dilewati memungkinkan penyisipan metadata yang ditentukan pengguna dalam aliran bingkai yang digabungkan. Struktur frame yang dapat dilewati adalah sebagai berikut.

|Nomor_ Ajaib |Ukuran_Bingkai |Data_Pengguna|
---|---|---|
|4 byte |4 byte |n byte|

## Referensi ##

* [Kompresi Standar RFC 8878](https://www.rfc-editor.org/rfc/rfc8878)


