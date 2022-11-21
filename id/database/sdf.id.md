{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "file sdf", "apa itu file sdf", "cara membuka file sdf", "ekstensi", "file", "format file sdf", "Tipe File Database", "Format File Database ", "File Basis Data" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file SDF dan API yang dapat membuat dan membuka file SDF.",
  "title" :"SDF - File Basis Data Ringkas SQL Server",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Apa itu file SDF?
File dengan ekstensi .sdf berisi database Microsoft SQL Server Compact (SQL CE) yang juga dikenal sebagai database relasional ringkas; diproduksi oleh Microsoft untuk aplikasi yang dibuat untuk perangkat seluler dan desktop. Ini mendukung sistem operasi 32 dan 64 bit dan konten database lengkap disertakan dalam satu file SDF dan dapat menempati lebih dari ruang disk 4GB. Untuk tujuan keamanan, file .sdf dapat dienkripsi dengan enkripsi 128-bit. Runtime SQL CE menyelesaikan akses multi-pengguna paralel ke file .sdf. File SDF dapat disalin melalui **QuickOnce** atau cukup disalin ke tujuan untuk penerapan sistem.

## Format File SDF
File SDF berisi database yang biasanya disebut database relasional kompak. File SDF berisi semua informasi terkait database dan SQL Server Compact adalah mesin database ringan dan gratis yang digunakan untuk mengelola file .sdf. Ukuran file .sdf tidak boleh melebihi batas ukuran 4 GB. File SDF tidak menyimpan informasi tentang prosedur tersimpan, pemicu, atau tampilan. Aplikasi yang menggunakan database SQL CE tidak perlu menentukan jalur ke file SDF di string koneksi ADO.NET, melainkan dapat disebut sebagai |DataDirectory|\database_name.sdf, yang mendefinisikan direktori data yang ditentukan dalam manifes rakitan untuk aplikasi
Konvensi penamaan .sdf bersifat opsional, dan ekstensi apa pun dapat digunakan untuk menyimpan file. Menyiapkan kata sandi untuk file database adalah langkah opsional. Untuk mengompres atau memperbaiki database, file harus disimpan dengan opsi **database yang dipadatkan/diperbaiki**.

## Referensi

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Menggunakan SQL Server Compact untuk Aplikasi Web ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


