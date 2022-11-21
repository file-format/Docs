{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file SQLITE dan API yang dapat membuat dan membuka file SQLITE.",
  "title" :"Format File SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Apa itu File SQLite?

File dengan ekstensi .sqlite adalah file database SQL ringan yang dibuat dengan software [SQLite](https://www.sqlite.org/index.html). Ini adalah database dalam file itu sendiri dan mengimplementasikan mesin database [SQL](/id/database/sql/) mandiri, berfitur lengkap, dan sangat andal. File database SQLite dapat digunakan untuk berbagi konten yang kaya antar sistem dengan hanya bertukar file ini melalui jaringan. Hampir semua ponsel dan komputer menggunakan SQLite untuk menyimpan dan berbagi data, dan merupakan pilihan format file untuk aplikasi lintas platform. Karena penggunaannya yang ringkas dan kegunaan yang mudah, ia dibundel di dalam aplikasi lain. Binding SQLite tersedia untuk bahasa pemrograman seperti C, [C#](/id/programming/cs), [C++](/id/programming/cpp), [Java](/id/programming/java/), [PHP](/id/programming/php/ ), dan banyak lagi.

## Format File SQLite

SQLite pada kenyataannya adalah pustaka Bahasa-C yang mengimplementasikan SQLite RDBMS menggunakan format file SQLite. Dengan evolusi perangkat baru setiap hari, format filenya tetap kompatibel mundur untuk mengakomodasi perangkat lama. Format file SQLite dipandang sebagai format arsip jangka panjang untuk data.

### Berkas Basis Data

Database SQLite dikelola sepenuhnya melalui dua file.
* File database utama - Berisi status lengkap dari database SQLite
* Rollback Journal - Menyimpan informasi tambahan dalam file kedua dan digunakan selama melakukan transaksi. Jika SQLite dalam mode WAL, file log kepala tulis dipertahankan.

#### File Jurnal

File ini dimaksudkan untuk menjaga agar semua informasi tetap terjaga jika transaksi terakhir tidak dapat diselesaikan dalam kasus seperti komputer crash. File ini digunakan untuk mengembalikan file database ke keadaan konsisten.

#### Halaman

File database SQLite utama terdiri dari satu atau lebih halaman. Setiap saat, setiap halaman dalam database utama memiliki satu penggunaan yang merupakan salah satu dari berikut ini:

* Halaman kunci-byte
* Halaman daftar gratis
* Halaman batang daftar bebas
* Halaman daun daftar bebas
* Halaman b-pohon
* Halaman interior tabel b-tree
* Sebuah tabel b-pohon halaman daun
* Halaman interior indeks b-tree
* Halaman daun b-tree indeks
* Halaman luapan muatan
* Halaman peta penunjuk

Ukuran file database SQLite dapat berkisar dari beberapa kilobyte hingga beberapa gigabyte.

### Tajuk SQLite

Header database SQLite terletak di 100 byte pertama dari file database. Setiap file database SQLite yang valid dimulai dengan 16 byte (dalam hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Rincian bidang header seperti pada tabel berikut.

|Offset|Ukuran|Deskripsi|
---|---|---|
|0|16|String tajuk: "format SQLite 3\000"|
|16|2|Ukuran halaman basis data dalam byte. Harus pangkat dua antara 512 dan 32768 inklusif, atau nilai 1 mewakili ukuran halaman 65536.|
|18|1|Format file tulis versi. 1 untuk warisan; 2 untuk WAL.|
|19|1|Format file baca versi. 1 untuk warisan; 2 untuk WAL.|
|20|1|Byte ruang "cadangan" yang tidak terpakai di akhir setiap halaman. Biasanya 0.|
|21|1|Fraksi muatan tersemat maksimum. Harus 64.|
|22|1|Minimal fraksi muatan tersemat. Harus 32.|
|23|1|Fraksi muatan daun. Harus 32.|
|24|4|Penghitung perubahan file.|
|28|4|Ukuran file database dalam halaman. "Ukuran database dalam header".|
|32|4|Nomor halaman dari halaman batang daftar bebas pertama.|
|36|4|Jumlah total halaman daftar bebas.|
|40|4|Kuki skema.|
|44|4|Nomor format skema. Format skema yang didukung adalah 1, 2, 3, dan 4.|
|48|4|Ukuran cache halaman standar.|
|52|4|Nomor halaman dari halaman akar b-tree terbesar saat dalam mode auto-vacuum atau incremental-vacuum, atau nol sebaliknya.|
|56|4|Pengkodean teks basis data. Nilai 1 berarti UTF-8. Nilai 2 berarti UTF-16le. Nilai 3 berarti UTF-16be.|
|60|4|"Versi pengguna" seperti yang dibaca dan disetel oleh pragma user_version.|
|64|4|True (bukan nol) untuk mode vakum inkremental. Salah (nol) sebaliknya.|
|68|4|"ID Aplikasi" yang ditetapkan oleh PRAGMA application_id.|
|72|20|Dicadangkan untuk ekspansi. Harus nol.|
|92|4|Versi-valid-untuk nomor.|
|96|4|SQLITE_VERSION_NUMBER|

## Referensi ##

* [Format File SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Spesifikasi Bahasa C](https://www.sqlite.org/c3ref/intro.html)

