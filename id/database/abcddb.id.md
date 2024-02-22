{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Pelajari tentang format file ABCDDB dan API yang dapat membuat dan membuka file ABCDDB.",
  "title" : "Format File ABCDDB - File Database Daftar Kontak Buku Alamat Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-id",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Apa itu file ABCDDB?

File dengan ekstensi **.ABCDDB** adalah singkatan dari Database Daftar Kontak Buku Alamat Apple. Itu milik aplikasi **Buku Alamat** yang juga dikenal sebagai **Kontak**. Ini adalah aplikasi bawaan dan disertakan dengan sistem operasi iOS dan macOS. Aplikasi Kontak memungkinkan pengguna untuk menyimpan dan mengatur informasi terkait kontak mereka, termasuk individu, bisnis, dan organisasi. Aplikasi ini memungkinkan pengguna untuk melacak detail seperti nama, alamat, nomor telepon, dan alamat email, serta mengkategorikan kontak mereka ke dalam grup.

## Hubungan dengan SQLite dan Jalur Khas

Buku Alamat Apple (juga dikenal sebagai Kontak) menyimpan informasi kontak sebagai vCard di folder metadata. **File _ABCDDB_ sebenarnya adalah _SQLite 3 datafile_**.

SQLite adalah sistem manajemen basis data populer yang dirancang ringan dan mandiri. Ini digunakan di berbagai jenis perangkat lunak dan perangkat. SQLite adalah jenis RDBMS, artinya menyimpan data dalam tabel yang terkait satu sama lain melalui kunci. Itu dapat menangani berbagai tipe data, termasuk bilangan bulat, angka floating-point, string, dan data biner. Selain itu, SQLite mendukung transaksi, yang memungkinkan pengguna melakukan beberapa operasi database secara bersamaan sebagai satu unit kerja.

File dengan ekstensi ABCDDB biasanya disimpan di sini

`~/Perpustakaan/Dukungan Aplikasi/Buku Alamat/Buku Alamat-v22.abcddb`

## Memperbaiki database Kontak yang rusak

Harap ambil cadangan terlebih dahulu sebelum mencoba melakukan ini. Kemudian silakan arahkan ke

`~/Perpustakaan/Dukungan Aplikasi/Buku Alamat`

Di direktori itu, Anda akan menemukan tiga file termasuk yang berekstensi .abcddb

- `buku alamat-v22.abcddb`
- `buku alamat-v22.abcddb-wal`
- `buku alamat-v22.abcddb-shm`

Hapus semua file ini dan buka kembali Kontak, itu akan mulai berfungsi kembali.

## Pulihkan database Buku Alamat dari Cadangan

Asumsikan, kontak basis data Buku Alamat Anda disimpan di `buku alamat-v22.abcddb`

- Pertama buat cadangan data Buku Alamat Anda dan keluar dari semua aplikasi.
- Pindahkan file database Anda ke subdirektori `~/Library/Application Support/AddressBook`
- Luncurkan **Buku Alamat.aplikasi**.

## Ekspor data file ABCDDB ke Microsoft Access

Karena file tersebut adalah file data SQLite 3, Anda dapat mengekspor data di dalam file abcddb ke Microsoft Access menggunakan konektor ODBC.

Konektor ODBC SQLite adalah pustaka perangkat lunak dan driver yang memungkinkan aplikasi yang mendukung antarmuka ODBC untuk menyambung ke database SQLite. Ini mencakup perpustakaan yang mendefinisikan antarmuka ODBC, dan driver yang menerjemahkan antarmuka ini menjadi panggilan ke API SQLite. Untuk menggunakan konektor ODBC SQLite, Anda harus menginstalnya terlebih dahulu lalu menyiapkan sumber data ODBC di komputer Anda. Setelah menyelesaikan langkah-langkah ini, aplikasi apa pun yang dilengkapi dengan dukungan ODBC akan dapat terhubung ke sumber data dan mengambil data dari database SQLite.

## Referensi
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Database Kontak Untuk Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Bagaimana cara membuka atau mengekspor file abcddb di Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

