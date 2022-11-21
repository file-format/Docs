{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file SQL dan API yang dapat membuat dan membuka file SQL.",
  "title" :"Format File SQL - File Data Bahasa Kueri Terstruktur",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Apa itu file SQL?

File dengan ekstensi .sql adalah file Structured Query Language (SQL) yang berisi kode untuk bekerja dengan database relasional. Ini digunakan untuk menulis pernyataan SQL untuk operasi CRUD (Buat, Baca, Perbarui, dan Hapus) pada database. File SQL umum digunakan saat bekerja dengan desktop serta database berbasis web. Ada beberapa alternatif SQL seperti Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL, dan beberapa lainnya. File SQL dapat dibuka oleh editor kueri Microsoft SQL Server, MySQL, dan editor teks biasa lainnya seperti Notepad di OS Windows.

## Sejarah Singkat

* Dikembangkan dan diperkenalkan oleh Donal D. Chamberlin dan Raymond F. Boyce di IBM pada awal 1970-an
* Digunakan untuk menyimpan dan mengambil data dari sistem manajemen database kuasi-relasional asli IBM, System R
* Mulai digunakan dalam basis produk komersial pada prototipe Sistem R mereka termasuk System/38, SQL/DS, dan DB2, yang tersedia secara komersial masing-masing pada tahun 1979, 1981, dan 1983.
* Diadopsi secara resmi oleh kelompok standar ANSI dan ISO sebagai standar "Database Language SQL" untuk sistem manajemen basis data relasional (RDBMS) pada tahun 1986

## Format File SQL

File SQL dalam format teks biasa dan dapat terdiri dari beberapa elemen bahasa. Beberapa pernyataan dapat ditambahkan ke satu file SQL jika eksekusinya dimungkinkan tanpa bergantung satu sama lain. Perintah SQL ini dapat dijalankan oleh editor kueri untuk menjalankan operasi CRUD.

### Elemen Bahasa SQL

Elemen bahasa SQL adalah seperti yang tercantum di bawah ini.

|Elemen|Deskripsi|
---|---|
|Klausul| Komponen penyusun pernyataan dan kueri.|
|Ekspresi| Dapat menghasilkan nilai skalar, atau tabel yang terdiri dari kolom dan baris data|
|Predikat| Tentukan kondisi yang dapat dievaluasi menjadi logika tiga nilai SQL (3VL) (benar/salah/tidak diketahui) atau nilai kebenaran Boolean dan digunakan untuk membatasi efek pernyataan dan kueri, atau untuk mengubah aliran program.|
|Pertanyaan| Mengambil data berdasarkan kriteria tertentu. Ini adalah elemen penting dari SQL.|
|Pernyataan| Dapat memiliki efek terus-menerus pada skemata dan data, atau dapat mengontrol transaksi, alur program, koneksi, sesi, atau diagnostik.|

### Contoh SQL
Pernyataan SQL berikut membuat tabel bernama **DATA**, diikuti dengan perintah `INSERT` tambahan untuk menyisipkan record dalam tabel ini.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referensi ##

* [SQL oleh Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Sintaks SQL](https://en.wikipedia.org/wiki/SQL_syntax)

