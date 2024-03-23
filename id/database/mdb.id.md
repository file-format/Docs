{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file MDB dan API yang dapat membuat dan membuka file MDB.",
  "title" :"Format File MDB - File Basis Data Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Apa itu file MDB?

File dengan ekstensi .mdb adalah file database Microsoft Access yang merupakan Relational Database Management System (RDBMS). Ini menyimpan data dalam tabel database yang ditautkan satu sama lain melalui kunci primer dan asing. File MDB berisi struktur lengkap dari tabel database, kueri, prosedur tersimpan. MDB adalah format file default untuk Microsoft Access 2003. Versi lateral Microsoft Access menggunakan format file [ACCDB](/id/database/accdb/) yang merupakan format file terbaru hingga saat ini. File MDB dapat dibuka dengan aplikasi seperti Microsoft Access, MDB Viewer, MDBOpener, dan dapat dikonversi ke format ACCDB, [CSV](/id/spreadsheet/csv/), Excel, dll.

## Format File MDB

Ada spesifikasi publik yang tersedia untuk format MDB dan tetap menjadi format file milik Microsoft. Microsoft, bagaimanapun, menyediakan akses konektivitas ke file MDB menggunakan standar Open Database Connectivity (ODBC) dan Visual Basic for Applications (VBA). Panduan MDB tidak resmi memberikan deskripsi informal singkat tentang format MDB berdasarkan rekayasa balik dan dapat dikonsultasikan untuk mengetahui tentang spesifikasinya.

### Halaman

Sesuai panduan MDB tidak resmi, file MDB terdiri dari halaman berukuran tetap (2048 byte untuk Jeb DB3 dan 4096 byte untuk Jet DB 4). Byte pertama menunjukkan jenis halaman. Berikut ini adalah jenis halaman kunci:

`Halaman Pertama:` Ini berisi informasi header database yang juga menyertakan identifikasi versi Jet DB yang kompatibel dengan file tersebut. Selain itu, juga mencakup informasi keamanan file dan peta penggunaan halaman.

`Halaman definisi tabel:` Halaman definisi tabel menentukan kolom, tipe data, indeks, dan informasi lainnya. Ini menggunakan halaman tambahan jika diperlukan dan menyertakan peta halaman yang berisi data baris untuk tabel ini.

`Halaman data:` Halaman data adalah wadah data aktual tempat data disimpan oleh baris. Ini menggunakan halaman tambahan untuk menyimpan nilai data yang panjang.

Satu database Microsoft Access dapat terdiri dari beberapa file yang memungkinkan untuk melebihi batasan ukuran file dan tabel. Ini memfasilitasi untuk meletakkan formulir dan kode dalam file MDB front-end di desktop pengguna dan data di file MDB backend lain di server yang terhubung ke jaringan.

## Referensi ##

* [Spesifikasi Akses](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
