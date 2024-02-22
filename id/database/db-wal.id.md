{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Pelajari tentang format file DB-WAL dan API yang dapat membuat dan membuka file DB-WAL.",
  "title" : "Format File DB-WAL - File Log Write-Ahead Database SQLite",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-id",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Apa itu file DB-WAL?

Ekstensi file .db-wal dikaitkan dengan SQLite, sistem manajemen basis data relasional sumber terbuka yang populer. Format file WAL (kependekan dari Write-Ahead Log) adalah alternatif dari jurnal rollback tradisional yang digunakan oleh SQLite. Ini memberikan lebih banyak kontrol konkurensi, memungkinkan beberapa proses membaca database pada saat yang sama, sambil tetap menyediakan kemampuan pemulihan kerusakan. File .db-wal digunakan untuk menyimpan perubahan yang dilakukan pada database yang belum dikomit ke file database utama (dengan ekstensi .db).

## Format WAL Umum

Dalam format file WAL (Write-Ahead Log), perubahan yang dilakukan pada database ditulis terlebih dahulu ke file WAL sebelum dikomit ke file database utama. Hal ini memungkinkan akses yang lebih bersamaan ke database, karena beberapa proses dapat membaca dari database saat perubahan sedang dilakukan. Selain itu, format file WAL menyediakan kemampuan pemulihan kerusakan, memungkinkan database dikembalikan ke keadaan sebelumnya jika terjadi pemadaman yang tidak terduga.

## Perbedaan antara format DB-WAL dan WAL

Format file .db-wal dan WAL dikaitkan dengan SQLite, sistem manajemen basis data relasional sumber terbuka yang populer. Namun, ada perbedaan halus di antara keduanya.

File .db-wal pada dasarnya adalah file WAL, tetapi dengan ekstensi file yang berbeda. File .db-wal digunakan untuk menyimpan perubahan yang dilakukan pada database yang belum dikomit ke file database utama (dengan ekstensi .db), sedangkan format file WAL digunakan untuk menyimpan log write-ahead dari perubahan database .

Dengan kata lain, file .db-wal adalah jenis file WAL khusus yang digunakan oleh database SQLite untuk menyimpan perubahan yang dibuat pada database yang belum dikomit ke file database utama. Format file WAL adalah istilah umum untuk jenis format file ini.

Jadi, WAL adalah istilah umum untuk format file, .db-wal adalah implementasi khusus dari format file WAL yang digunakan oleh database SQLite.

## Referensi
* [Format File mode WAL](https://www.sqlite.org/walformat.html)

* [Pencatatan Log Awal](https://www.sqlite.org/wal.html)


