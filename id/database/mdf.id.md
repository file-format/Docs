{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file MDF dan API yang dapat membuat dan membuka file MDF.",
  "title" :"Format File MDF - File Database Master SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file MDF?

File dengan ekstensi .mdf adalah File Database Master yang digunakan oleh [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) untuk menyimpan data pengguna. Ini sangat penting karena semua data disimpan dalam file ini. File MDF menyimpan data pengguna dalam database relasional dalam bentuk kolom, baris, bidang, indeks, tampilan, dan tabel. SQL Server memungkinkan untuk mengatur pengaturan autogrow dan autoshrink agar berdampak positif pada kinerja database. File MDF dapat dimuat dan dilampirkan ke database menggunakan Microsoft SQL Server. File MDF memiliki tipe mime Application/octet-stream.

## Format File MDF

Unit dasar penyimpanan data di SQL Server adalah halaman. Halaman penyimpanan yang ditetapkan database dibagi menjadi halaman logis yang diberi nomor dari 0 hingga n. Satu halaman dimulai dengan header 96 byte yang terdiri dari ID Halaman, jenis struktur halaman, jumlah catatan di halaman, dan penunjuk ke halaman sebelumnya dan berikutnya.

### Struktur Berkas

File MDF memiliki struktur data berikut.

* Halaman 0: Tajuk
* Halaman 1: PFS pertama
* Halaman 2: GAM Pertama
* Halaman 3: SGAM Pertama
* Halaman 4: Tidak digunakan
* Halaman 5: Tidak digunakan
* Halaman 6: DCM Pertama
* Halaman 7: BCM Pertama

#### Kepala Berkas

Nomor halaman 0 dari semua file berisi header yang menyimpan metadata tentang file tersebut.

#### Ruang Kosong Laman (PFS)
PFS mengidentifikasi status alokasi dan menentukan jumlah ruang kosong.

* Bit 1: Menunjukkan apakah halaman dialokasikan atau tidak.
* Bit 2: Menunjukkan jika halaman berasal dari campuran.
* Bit 3: Menunjukkan bahwa halaman ini adalah halaman IAM.
* Bit 4: Menunjukkan bahwa halaman ini berisi ghost record
* Bit 5 hingga 7: Nilai gabungan tiga bit, yang menunjukkan kepenuhan halaman sebagai berikut:
* 0: Halaman kosong
* 1: Halaman terisi 1–50%.
* 2: Halaman 51–80% penuh
* 3: Halaman 81–95% penuh
* 4: Halaman 96–100% penuh

## Referensi

* [File dan Grup File Database](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Lepas dan Lampirkan Basis Data - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Menganalisis Anatomi File Data SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

