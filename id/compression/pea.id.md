{
  "date" : "2021-04-21",
  "keywords" :[ "file kacang", "format file kacang", "apa itu file kacang", "file", "contoh kacang", "ekstensi file kacang", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Format File Arsip PeaZip",
  "description":"Pelajari tentang format file PEA dan API yang dapat membuat dan membuka file PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Apa itu file PEA?

File dengan ekstensi .pea, singkatan dari Kemas, Enkripsi, dan Autentikasi, adalah arsip [zip](/id/compression/zip/) yang dibuat dengan aplikasi perangkat lunak pengarsipan [PeaZip](https://peazip.github.io/). Ini fitur kompresi dan output volume ganda, dan menawarkan model keamanan yang fleksibel melalui Enkripsi dan kriptografi yang diautentikasi. Ini memberikan privasi dan otentikasi data. Utilitas PeaZip tersedia sebagai mesin sumber terbuka yang dapat dikompilasi untuk berbagai OS sesuai kebutuhan.

## Format File PEA

[Spesifikasi format file PEA](https://peazip.github.io/pea_help.pdf) tersedia untuk umum sebagai referensi developer. Arsip PEA adalah file biner dengan model keamanan yang fleksibel dan pemeriksaan integritas yang berlebihan mulai dari checksum hingga hash yang kuat secara kriptografis. Ini mendefinisikan tiga tingkat komunikasi yang berbeda untuk dikendalikan:

* Streams - aliran data output aktual yang dibentuk oleh banyak file input dan dapat ditulis ke beberapa volume output
* Objek - masukkan file dan folder yang dikirim ke arsip .pea
* Volume - file arsip keluaran yang dapat direntang ke ukuran yang ditentukan pengguna

Masing-masing bersifat opsional dan dapat digabungkan sesuai kebutuhan pengguna. Format file PEA dapat menyimpan satu aliran yang berisi objek tak terbatas. Setiap aliran berukuran hingga 2^64 byte.

File PEA menawarkan pemeriksaan integritas opsional dan enkripsi yang diautentikasi menggunakan AES dalam mode EAX atau HMAC, atau Twofish dan Serpent dalam mode EAX.

### Tajuk Arsip PEA

Header arsip adalah 10 byte dan disusun sebagai berikut.

|Byte|Deskripsi|
---|---|
|1 | Bidang byte ajaib untuk disambiguasi format file: $EA|
|1 | Nomor Versi|
|1 | Nomor Revisi|
|1 | Skema kontrol volume|
|1 | Mendeklarasikan OS tempat aliran dibuat|
|1 | Mendeklarasikan enkode tanggal dan waktu OS|
|1 | Mendeklarasikan pengkodean karakter nama objek|
|1 | Mendeklarasikan tipe CPU (dikodekan dalam 7 bit) dan endianness (dalam msb)|
|1 | Dicadangkan untuk penggunaan mendatang|

## Referensi

* [Spesifikasi Format File PEA](https://peazip.github.io/pea_help.pdf)
* [Format File PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

