{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File STR - File Objek Daftar Struktur dBASE - Apa itu file .str dan bagaimana cara membukanya?",
  "description" : "Pelajari tentang File Objek Daftar Struktur STR dBASE dan cara membukanya.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-id",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Apa itu file STR?

Format file STR umumnya dikaitkan dengan dBASE, sistem manajemen basis data. Di dBASE, file .str biasanya mewakili file objek daftar struktur. File ini berisi struktur tabel database, termasuk informasi tentang field (kolom) dan propertinya.

File objek daftar struktur (.str) berisi metadata seperti nama bidang, tipe data, panjang bidang, dan properti lain yang terkait dengan setiap bidang dalam tabel database. Ini digunakan untuk mendefinisikan struktur tabel database tanpa berisi catatan data aktual.

Program seperti dBASE atau alat manajemen basis data lainnya dapat memanfaatkan file ini untuk memahami tata letak tabel basis data dan melakukan operasi seperti membuat kueri, memperbarui, atau membuat catatan baru berdasarkan struktur ini.

Berikut adalah contoh dasar isi file STR:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Contoh ini menjelaskan tabel dengan empat bidang: ID, Nama, Usia, dan DOB, beserta tipe data dan panjangnya masing-masing.

## Bagaimana cara membuka file STR?

Cara utama untuk membuka file .str adalah dengan menggunakan dBASE itu sendiri, khususnya pada sistem operasi Windows. dBASE mampu membaca dan menafsirkan konten file-file ini, memungkinkan pengguna untuk melihat dan bekerja dengan struktur database.

Karena file .str pada dasarnya adalah file teks biasa yang berisi informasi tentang struktur database, Anda juga dapat membukanya menggunakan editor teks. Contoh editor teks termasuk Microsoft Notepad di Windows dan Apple TextEdit di Mac. Saat dibuka di editor teks, Anda akan dapat melihat konten file, termasuk nama field, tipe data, dan informasi struktural lainnya, dalam format yang dapat dibaca manusia.

## Referensi
* [dBase](https://en.wikipedia.org/wiki/DBase)


