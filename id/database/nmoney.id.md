{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file NMONEY dan API yang dapat membuat dan membuka file NMONEY.",
  "title" :"File NMONEY - Format File Akun Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Apa itu file NMONEY?

File NMONEY adalah file database penyimpanan data keuangan yang berisi rekam jejak transaksi keuangan. Ini dikembangkan oleh Nickvision dan digunakan dalam perangkat lunak Nickvision Denaro yang merupakan aplikasi perangkat lunak keuangan pribadi. Data yang disimpan dalam file NOMONEY mencakup informasi transaksi kredit dan debit ke suatu rekening.

File NOMONEY dapat dibuka dengan aplikasi [Github](https://github.com/NickvisionApps/Denaro).

## Tentang Perangkat Lunak Denaro

Denaro awalnya dikembangkan oleh [Nickvision](https://nickvision.org/) sebagai produk yang kemudian diubah menjadi aplikasi perangkat lunak sumber terbuka yang dihosting di [Github](https://github.com/NickvisionApps/Denaro) . Sejak itu aplikasi telah dimodifikasi dan diperbarui hanya di Github. Aplikasi ini dikembangkan dalam C# di Windows UI dengan Windows App SDK (WinUI 3 seperti saat ini).

### Fitur yang Ditawarkan oleh Denaro

* Kelola banyak akun secara bersamaan dengan antarmuka tab yang paling populer dan familiar
* Filter transaksi berdasarkan jenis, grup, atau tanggal
* Mengulangi transaksi seperti tagihan yang terjadi setiap bulannya
* Transfer uang dari satu rekening ke rekening lainnya
* Ekspor data dari akun sebagai file CSV dan impor file CSV, OFX atau QIF untuk menambahkan transaksi ke akun

## Format File Denaro - Informasi Lebih Lanjut

File Denaro disimpan ke disk dalam format file biner. Data keuangan disimpan sebagai file database dalam format file **.SQLITE3**. SQLITE adalah file database SQL ringan yang dibuat dengan perangkat lunak SQLite. Ini menyediakan mesin basis data mandiri yang mampu menyediakan basis data berfitur lengkap dan sangat andal. File database SQLite dapat digunakan untuk berbagi konten yang kaya antar sistem hanya dengan bertukar file ini melalui jaringan. Pengikatan SQLite ada untuk bahasa pemrograman seperti C, [C#](/id/programming/cs/), [C++](/id/programming/cpp/), [Java](/id/programming/java/), [PHP](/id/programming/ php/), dan masih banyak lainnya.

## Referensi

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

