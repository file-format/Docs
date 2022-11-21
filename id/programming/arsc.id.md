{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "apa itu file arsc", "cara membuka file arsc", "ekstensi", "file", "file arsc", "format file arsc", "ekstensi file arsc" ,"Contoh Berkas arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - File Tabel Sumber Daya Paket Android",
  "description":"Pelajari tentang format file ARSC dan API yang dapat membuat dan membuka file ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Apa itu file ARSC?

File ARSC adalah file tabel Sumber Daya Android yang berisi daftar sumber daya aplikasi dalam format tabel. Ini berisi informasi seperti nama Resource, properti, dan ID. File ARSC adalah bagian dari paket APK yang digunakan untuk menginstal aplikasi Android ini. Semua sumber daya seperti gambar, tata letak, gaya, dan string, dalam aplikasi android diubah menjadi file biner saat file APK dibuat. File ARSC juga dihasilkan pada saat yang sama, berisi daftar semua sumber daya program yang dikompilasi dan ID mereka.

## Format File ARSC

File ekstensi .arsc adalah file biner yang dibuat setelah compiler, seperti ANT (Eclipse) atau Gradle (AS), mengkompilasi kode aplikasi Android untuk menghasilkan file [APK](/id/compression/apk/). Anda dapat mengekstrak file APK menggunakan utilitas pengarsipan apa pun seperti WinZip untuk melihat kontennya, yang merupakan file kelas java yang dikompilasi yaitu class.dex. Selain itu, ini juga berisi file ARSC yang berisi informasi meta tentang:

* Node XML
* Atribut
* ID Sumber Daya

Sumber daya dalam file APK dirujuk oleh ID Sumber Daya, sedangkan atribut diselesaikan ke nilai pada waktu proses. Alat aapt Android mengumpulkan semua sumber daya yang ditentukan dalam file pada waktu pembuatan dan menetapkan ID sumber daya untuknya. Setelah pengidentifikasi ditugaskan ke sumber daya yang dikompilasi, file R.java dihasilkan dari kode sumber serta resources.arsc.

## Referensi

* [Struktur Tabel Sumber Daya Biner](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

