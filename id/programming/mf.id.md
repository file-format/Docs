{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Format File Manifes Java",
  "description":"Pelajari tentang format file MF dan API yang dapat membuat dan membuka file MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file MF?

File dengan ekstensi .mf adalah file Manifes Java yang berisi informasi tentang setiap entri file [JAR](/id/programming/jar/). File MF itu sendiri terdapat di dalam file JAR dan menyediakan semua ekstensi dan definisi terkait paket. File JAR dapat diproduksi untuk digunakan sebagai file yang dapat dieksekusi. Dalam kasus seperti itu, file mainfest menentukan kelas utama aplikasi yang berisi pernyataan **`public static void main`**. File manifes diberi nama MANIFEST.MF dan dapat dibuka dengan editor teks apa pun di Sistem Operasi Windows, MacOS dan Linux.

## Spesifikasi Format File Manifes

[Spesifikasi format file manifes](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) tersedia oleh Oracle dalam panduan mereka untuk format file JAR. File Manifest terdiri dari bagian utama yang diikuti oleh daftar bagian untuk setiap entri file JAR. Setiap bagian mengikuti beberapa aturan dan batasan.

### Bagian Utama

Bagian utama:

* berisi informasi tentang keamanan dan konfigurasi tentang file JAR
* berisi informasi tentang aplikasi atau ekstensi yang menjadi bagian dari file JAR
* menentukan atribut utama untuk setiap item manifes individual

**Catatan**: Tidak ada atribut di bagian ini yang dapat diberi nama "Nama".

### Bagian Individu

Bagian individual menentukan berbagai atribut untuk paket atau file dari file JAR. Setiap bagian harus dimulai dengan atribut bernama "Nama" yang nilainya harus berupa jalur relatif ke file, atau URL absolut yang mereferensikan data di luar arsip.

### Spesifikasi Manifes

|Atribut|Deskripsi|
---|---|
|file manifes|baris baru bagian utama *bagian-individu|
|bagian-utama|info-versi baris baru *atribut-utama|
|info-versi|Versi-Manifes : nomor-versi|
|nomor-versi|digit+{.digit+}*|
|main-attribute|(semua atribut utama yang sah) baris baru|
|individual-section|Name : nilai baris baru *perentry-attribute|
|perentry-attribute|(setiap atribut perentry yang sah) baris baru|
|baris baru|CR LF | JIKA | CR (tidak diikuti oleh LF)|
|angka|{0-9}|

## Referensi

* [Oracle - Format File JAR](https://docs.Oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Format File JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

