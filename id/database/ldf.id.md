{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file LDF dan API yang dapat membuat dan membuka file LDF.",
  "title" :"LDF - Format File Basis Data Master SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file LDF?

File dengan ekstensi .ldf adalah file log yang dikelola oleh Microsoft SQL Server yang merupakan sistem manajemen basis data relasional (RDBMS). Semua transaksi yang dilakukan pada file database utama ([MDF](/id/database/mdf/))(seperti penyisipan, pembaruan, penghapusan) dicatat dalam file LDF. File LDF adalah komponen penting dari database apa pun. Jika terjadi kegagalan sistem, file log digunakan untuk mengembalikan database ke keadaan yang konsisten. File log transaksi dapat bertambah besar jika transaksi tidak dilakukan sepenuhnya. File LDF dapat dibuka dengan aplikasi perangkat lunak Microsoft SQL Server.

## Operasi Direkam dalam File LDF

File log SQL merekam operasi berikut:

* Awal dan akhir setiap transaksi.

* Setiap modifikasi data data (masukkan, perbarui, atau hapus). Ini juga termasuk perubahan oleh prosedur tersimpan sistem atau pernyataan bahasa definisi data (DDL) ke tabel apa pun, termasuk tabel sistem.

* Setiap tingkat dan alokasi halaman atau deallocation.

* Membuat atau menjatuhkan tabel atau indeks.

## Format File LDF

File LDF terdiri dari catatan transaksi SQL Server yang disusun sebagai rangkaian catatan log. Setiap log record memiliki log sequence number (LSN) yang lebih tinggi dari LSN record sebelumnya. String digabungkan setelah satu sama lain dalam file. Karena komputer kecepatan tinggi modern, catatan dapat disisipkan di mana LSN2 ada di file log sebelum LSN1. Karena operasi dicatat dalam serial, perubahan yang dijelaskan oleh LSN2 dilakukan setelah catatan log LSN1. Catatan untuk transaksi tertentu ditautkan ke belakang menggunakan penunjuk yang digunakan dan mempercepat pengembalian transaksi.
 

## Referensi

* [File dan Grup File Database](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Panduan Manajemen dan Arsitektur Log Transaksi](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- server-ver15)

