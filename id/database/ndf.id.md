{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file MDF dan API yang dapat membuat dan membuka file NDF.",
  "title" :"Format File NDF - File Database Master SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file NDF?

File dengan ekstensi .ndf adalah file database sekunder yang digunakan oleh [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) untuk menyimpan data pengguna. NDF adalah file penyimpanan sekunder karena server SQL menyimpan data yang ditentukan pengguna dalam file penyimpanan utama yang dikenal sebagai [MDF](/id/database/mdf/). File data NDF bersifat opsional dan ditentukan pengguna untuk mengelola penyimpanan data jika file MDF utama menggunakan semua ruang yang dialokasikan. Biasanya disimpan pada disk terpisah dan dapat menyebar ke beberapa perangkat penyimpanan. Kehadiran file MDF diperlukan untuk membuka file NDF.

## Format File NDF

Format file NDF tidak berbeda dengan [MDF](/id/database/mdf/) dan menggunakan halaman sebagai unit dasar penyimpanan data. setiap halaman dimulai dengan header 96 byte yang mencakup:

* ID halaman
* Jenis Struktur
* Jumlah catatan di halaman
* Pointer ke halaman sebelumnya dan berikutnya

### Struktur Berkas NDF

File MDF memiliki struktur data berikut.

* Halaman 0: Tajuk
* Halaman 1: PFS pertama
* Halaman 2: GAM Pertama
* Halaman 3: SGAM Pertama
* Halaman 4: Tidak digunakan
* Halaman 5: Tidak digunakan
* Halaman 6: DCM Pertama
* Halaman 7: BCM Pertama

#### Tajuk Berkas NDF

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

## Halaman Berkas Data

Halaman dalam file data SQL Server dimulai dari nol (0) dan bertambah secara berurutan. Setiap file dikenali dengan nomor ID file yang unik. Pasangan ID file dan nomor halaman secara unik mengidentifikasi halaman dalam database. Contoh menunjukkan nomor halaman dalam database, adalah seperti pada gambar berikut.

{{< figure src="../ndf.png" alt="Format File Basis Data NDF" >}}

Contoh ini memperlihatkan nomor halaman dalam database yang memiliki file data primer 4 MB dan file data sekunder 1 MB.

## Referensi

* [File dan Grup File Database](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Lepas dan Lampirkan Basis Data - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Menganalisis Anatomi File Data SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

