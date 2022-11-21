{
  "date" : "2021-04-08",
  "keywords" :[ "file lz", "format file lz", "apa itu file lz", "file", "contoh lz", "ekstensi file lz", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File Terkompresi LZ - Lzip",
  "description":"Pelajari tentang format file LZ dan API yang dapat membuat dan membuka file LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Apa itu file LZ?

File dengan ekstensi .lz adalah file arsip terkompresi yang dibuat dengan Lzip, yang merupakan alat baris perintah gratis untuk kompresi. Ini mendukung penggabungan untuk mengompres file dukungan. File LZ memiliki jenis media application/lzip dan mendukung rasio kompresi yang lebih tinggi daripada [BZ2](/id/compression/bz2). LZ didasarkan pada algoritme LZMA (rantai Lempel-Ziv-Markov) dan menyertakan checksum CRC 32-bit dan byte ident untuk memeriksa integritas file.

## Format Terkompresi LZMA

Format terkompresi LZMA terdiri dari aliran bit terkompresi yang dikodekan menggunakan koder rentang biner adaptif. Aliran dibagi menjadi paket-paket. Setiap paket menggambarkan satu byte atau urutan LZ77. Panjang dan jarak setiap paket dikodekan secara implisit atau eksplisit.

Ketujuh jenis paket tersebut adalah sebagai berikut ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Kode yang dikemas (urutan bit) |Nama paket |Deskripsi paket|
---|---|---|
|0 + byteCode| LIT| Satu byte yang disandikan menggunakan pembuat kode rentang biner adaptif.|
|1+0 + len + dist| PERTANDINGAN| Urutan LZ77 tipikal yang menjelaskan panjang dan jarak urutan.|
|1+1+0+0| SINGKAT| Urutan LZ77 satu byte. Jarak sama dengan jarak LZ77 yang terakhir digunakan.|
|1+1+0+1 + len| LONGREP[0]| Urutan LZ77. Jarak sama dengan jarak LZ77 yang terakhir digunakan.|
|1+1+1+0 + len| LONGREP[1]| Urutan LZ77. Jarak sama dengan jarak LZ77 kedua yang terakhir digunakan.|
|1+1+1+1+0 + len| LONGREP[2]| Urutan LZ77. Jarak sama dengan jarak LZ77 ketiga yang terakhir digunakan.|
|1+1+1+1+1 + len| LONGREP[3]| Urutan LZ77. Jarak sama dengan jarak keempat LZ77 yang terakhir digunakan.|


## Referensi

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

