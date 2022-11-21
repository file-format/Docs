{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DDL dan API yang dapat membuat dan membuka file DDL.",
  "title" :"Format File DDL - File Bahasa Definisi Data",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Apa itu file DDL?

File dengan ekstensi .ddl adalah file Bahasa Definisi Data yang digunakan untuk menentukan skema database. Ini berisi pernyataan/perintah untuk bekerja dengan struktur basis data seperti tabel, kolom, catatan, dan bidang lainnya. Perintah dalam file DDL ditulis dalam [SQL](/id/database/sql/) dan dapat melakukan operasi seperti membuat tabel di database, menghapus, dan memperbarui. Skema basis data dimiliki oleh yang dibuatnya dan semua operasi CRUD dapat dilakukan di atasnya. Aplikasi populer yang dapat membuat dan membuka file DDL adalah Windows Text Editor, Jetbrains Intellij Idea, dan EclipseLink.

## perintah DDL

Satu file DDL dapat berisi beberapa perintah yang, karena sintaks yang benar, akan dieksekusi secara berurutan dan membuat perubahan pada skema seperti membuat set karakter dan tabel, menjatuhkan tabel, mengganti nama dan mengubah tabel. Mengikuti perintah DDL biasanya digunakan saat bekerja dengan skema database.

`CREATE` - Digunakan untuk membuat database atau objeknya (seperti tabel, indeks, fungsi, tampilan, prosedur penyimpanan, dan pemicu).

`DROP` – Digunakan untuk menghapus objek dari database.

`ALTER` - Digunakan untuk mengubah struktur database.

`TRUNCATE` – Digunakan untuk menghapus semua catatan dari tabel, termasuk semua ruang yang dialokasikan untuk catatan dihapus.

`COMMENT` – Menambahkan komentar ke kamus data.

`RENAME` – Mengganti nama objek yang ada di database.

## Contoh DDL

Contoh berikut menunjukkan pernyataan DDL untuk perintah CREATE yang membuat tabel dan menentukan bidangnya.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referensi ##

* [DDL oleh Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

