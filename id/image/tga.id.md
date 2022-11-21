{
  "date" : "2019-10-11",
  "keywords" :[ "file tga", "format file tga", "apa itu file tga", "file", "contoh tga", "ekstensi file tga", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File TGA - File Gambar Grafis TARGA",
  "description":"Pelajari tentang format file TGA dan API yang dapat membuat dan membuka file TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file TGA?

File dengan ekstensi .tga adalah format grafik raster dan dibuat oleh Truevision Inc. File ini dirancang untuk board TARGA (Truevision Advanced Raster Adapter) dan memberikan dukungan tampilan Highcolor/truecolor untuk PC yang kompatibel dengan IBM. Ini mendukung 8, 16, 24 dan 32 bit per piksel dan saluran alfa 8-bit. Ini juga mendukung kompresi RLE lossless yang dapat diterapkan untuk mengurangi ukuran gambar. Foto dan tekstur digital menggunakan format gambar TGA.

## Sejarah Singkat

Pembentukan format file TGA muncul pada tahun 1984 oleh AT&T EPICenter (kemudian diekstraksi dan dibentuk sebagai entitas independen yang dikenal sebagai Truevision) yang sedang mengerjakan pemasaran teknologi baru yang dikembangkan oleh AT&T untuk buffer bingkai warna. EPICenter sudah mengerjakan dua kartu pertamanya, VDA (Video Display Adapter) dan ICB (image capture board) yang bekerja pada dua jenis file, .vda dan .icb, sudah dalam proses. Format file ini dikodifikasi dan format file spesifik yang kurang luas TGA diperkenalkan. TGA adalah perpanjangan dari apa yang sudah digunakan, dan memberikan informasi seperti lebar, tinggi, kedalaman piksel, peta warna terkait, dan asal gambar.

Versi 2.0 TGA, diterbitkan pada tahun 1989, menggabungkan beberapa fitur yang disempurnakan seperti:

* Gambar mini
* Saluran alfa
* Nilai Gamma
* Metadata Tekstual

Kontributor utama untuk versi 2.0 TGA termasuk Shawn Steiner dari Truevision, Kevin Fiedly dan David Spoelstra.

## Spesifikasi Format File TGA TARGA

File TGA terdiri dari 2 bagian utama:

* Tajuk
* Informasi Piksel Warna

Semua nilai dalam file TGA dalam littl-endian sesuai spesifikasi format.

### Tajuk TGA

Header file TGA terdiri dari 5 bidang berikut.

|No bidang.|Panjang |Nama bidang |Deskripsi|
---|---|---|---|
|1| 1 byte |panjang ID| Panjang kolom ID gambar (0-255)|
|2| 1 byte |Jenis peta berwarna| Apakah peta warna disertakan (0 - menunjukkan bahwa tidak ada data peta warna yang disertakan dengan gambar ini. 1 - menunjukkan bahwa peta warna disertakan dengan gambar ini.)|
|3| 1 byte |Jenis gambar| Jenis kompresi dan warna (0- Tidak Termasuk Data Gambar. 1- Tidak terkompresi, Gambar yang dipetakan berwarna, 2- Tidak terkompresi, Gambar True Color, 9- Panjang proses disandikan, Gambar dipetakan berwarna, 11- Jalan-Panjang disandikan, Gambar hitam dan putih )|
|4| 5 byte |Spesifikasi peta warna| Menjelaskan peta warna|
|5| 10 byte | Spesifikasi gambar| Dimensi dan format gambar|

### Gambar dan Data Peta Warna

|No bidang. |Panjang |Bidang |Deskripsi|
---|---|---|---|
|6 |Dari bidang panjang ID gambar| ID Gambar| Bidang opsional yang berisi informasi pengenal|
|7 |Dari bidang spesifikasi peta warna| Data peta warna| Tabel pencarian yang berisi data peta berwarna|
|8 |Dari bidang spesifikasi gambar| Data gambar| Disimpan sesuai dengan deskriptor gambar|

### Area Pengembang (Opsional)

TGA Versi 2.0 menyediakan dukungan untuk penyempurnaan/ekstra tambahan yang diinginkan oleh banyak pengembang untuk menyimpan lebih banyak informasi. Informasi bersifat opsional sehingga jika dekoder TGA tidak dapat menafsirkannya, maka akan diabaikan.

### Area Ekstensi (Opsional)

|No bidang.| Panjang| Kolom |Deskripsi|
---|---|---|---|
|10| 2 byte |Ukuran ekstensi |Ukuran dalam byte area ekstensi, selalu 495|
|11| 41 byte| Nama penulis | Nama penulis. Jika tidak digunakan, byte harus diset ke NULL (\0) atau spasi|
|12| 324 byte| Komentar penulis| Sebuah komentar, diatur dalam empat baris, masing-masing terdiri dari 80 karakter ditambah NULL|
|13| 12 byte| Stempel tanggal/waktu |Tanggal dan waktu pembuatan gambar|
|14| 41 byte| ID Pekerjaan||
|15| 6 byte| Waktu kerja| Jam, menit, dan detik dihabiskan untuk membuat file (untuk penagihan, dll.)|
|16| 41 byte| ID Perangkat Lunak |Aplikasi yang membuat file.|
|17| 3 byte| Versi perangkat lunak||
|18| 4 byte| Warna kunci||
|19| 4 byte| Rasio tinggi lebar piksel||
|20| 4 byte| Nilai gamma||
|21| 4 byte| Offset koreksi warna |Jumlah byte dari awal file ke tabel koreksi warna jika ada|
|22| 4 byte| perangko | Jumlah byte dari awal file ke gambar prangko jika ada|
|23| 4 byte| Pindai garis offset| Jumlah byte dari awal file ke tabel garis pindai jika ada|
|24| 1 byte| Jenis atribut| Menentukan saluran alfa|

### File Footer (Opsional)

26 byte terakhir dari file mewakili footer, yang jika ada berarti kemungkinan file TGA versi 2.

|Nomor Lapangan| Panjang| bidang| Deskripsi|
---|---|---|---|
|28| 4 byte| Offset ekstensi| Offset dalam byte dari awal file|
|29| 4 byte| Offset area pengembang| Offset dalam byte dari awal file|
|30| 16 byte| Tanda tangan| Berisi "TRUEVISION-XFILE"|
|31| 1 byte| | Berisi "."|
|32| 1 byte| | Berisi NULL|


## Referensi

* [Spesifikasi Format File TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA oleh Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

