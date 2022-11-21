{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File GDB - File Geodatabase File ESRI",
  "description":"Pelajari tentang format file GDB dan API yang dapat membuat dan membuka file GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Apa itu file GDB?

File ESRI Geodatabase (FileGDB) adalah kumpulan file dalam folder pada disk yang menyimpan data geospasial terkait seperti kumpulan data fitur, kelas fitur, dan tabel terkait. Itu membutuhkan file lain tertentu untuk disimpan di samping file .gdb di direktori yang sama agar bisa berfungsi. Kueri dapat dijalankan pada file .gdb untuk mengelola data spasial maupun non-spasial.

## Format File GDB - Informasi Lebih Lanjut

File geodatabases terdiri dari tujuh tabel sistem ditambah data pengguna. Data pengguna dapat disimpan dalam jenis kumpulan data berikut:

* Kelas fitur
* Kumpulan data fitur
* Kumpulan data mosaik
* Katalog raster
* Kumpulan data raster
* Kumpulan data skematis
* Tabel (nonspasial)
* Kotak alat

Kumpulan data fitur dapat berisi kelas fitur serta jenis kumpulan data berikut:

* Lampiran
* Anotasi terkait fitur
* Jaringan geometris
* Kumpulan data jaringan
* Paket kain
* Kelas hubungan
* Medan
* Topologi

Ukuran maksimum default dari kumpulan data dalam file geodatabases adalah 1 TB. Ukuran maksimum dapat ditingkatkan menjadi 256 TB untuk kumpulan data besar (biasanya raster). Ini dikendalikan oleh kata kunci konfigurasi. Lihat Kata kunci konfigurasi untuk file geodatabases untuk informasi lebih lanjut.

File geodatabases juga dapat berisi subtipe dan domain dan berpartisipasi dalam replikasi checkout/check-in dan replika satu arah.

Sebuah file geodatabase dapat diakses secara bersamaan oleh beberapa pengguna. Jika pengguna mengedit, mereka harus mengedit kumpulan data yang berbeda.

## Spesifikasi Format File GDB ##

File GDB adalah format berpemilik ESRI dan spesifikasinya tidak tersedia untuk umum. Karena alasan ini, detail format file untuk FIle GDB tidak dapat didokumentasikan di mana pun selain beberapa sumber yang telah melakukannya [sebagian](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) dengan rekayasa terbalik .

## Referensi ##

* [Spesifikasi FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

