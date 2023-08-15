{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file ACCDB dan API yang dapat membuat dan membuka file ACCDB.",
  "title" :"Format File ACCDB - File Basis Data Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Apa itu file ACCDB?

File dengan ekstensi .accdb adalah file database Microsoft Access 2007 yang menyimpan data pengguna dalam tabel. Ini mendukung penyimpanan
formulir kustom, kueri SQL, dan data lainnya. File ACCDB menggantikan file [MDB](/id/database/mdb/) setelah Microsoft beralih ke struktur file berbasis XML. File ACCDB masih dapat dikonversi ke MDB dengan kompatibilitas lama. Namun, ACCDB adalah format file database Access yang banyak digunakan sekarang. Microsoft juga mendukung fitur tambahan dalam format ACCDB seperti kemungkinan menyimpan lampiran file, data biner, dan dukungan bidang multi-nilai.

## Format File ACCDB

Seperti MDB, tidak ada spesifikasi publik yang tersedia untuk format file ACCDB. Microsoft mendukung pengaksesan file ini secara terprogram melalui standar Open Database Connectivity (ODBC) dan Visual Basic for Applications (VBA).

### Sebuah Wawasan

Dump hex dari file ACCDB sederhana menunjukkan bahwa ada kesamaan umum dalam struktur dengan versi terbaru Keluarga Format MDB pendahulunya. Kedua format file menggunakan ukuran halaman tetap sebesar 4096 byte. Kesamaan lain antara ACCDB dan MDB adalah bentuk angka ajaib, yang menyertakan string "Standard ACE DB" untuk ACCDB. Versi atau kode kompatibilitas berada di lokasi yang sama di kedua format. mdbtools | File HACKING menyatakan "Offset 0x14 berisi versi Jet dari database ini" dan Panduan MDB tidak resmi setuju. Informasi dalam sumber ini, digabungkan dengan entri Wikipedia untuk [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), menunjukkan bahwa nilai 0x02 menunjukkan ACE 12 (Access 2007) dan 0x03 menunjukkan ACE 14 (Akses 2010). Namun, database minimal yang dibuat di Access 2010 dan database serupa yang dibuat di Access 2016 keduanya memiliki 0x02 di lokasi ini. Database minimal yang dibuat di Access 2016, tetapi menentukan kolom dengan tipe data "integer besar" yang baru diperkenalkan, memiliki nilai 0x05. Dalam file ACCDB, indikator ini tampaknya mencerminkan kompatibilitas file daripada versi mesin ACE yang digunakan untuk membuatnya.

## Referensi

* [Akses Spesifikasi 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Mesin Basis Data Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Format file Access mana yang harus saya gunakan?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
