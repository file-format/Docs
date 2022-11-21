{
  "date" : "2019-10-11",
  "keywords" :[ "file apk", "format file apk", "apa itu file apk", "file", "contoh apk", "ekstensi file apk", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Apa itu file APK?",
  "description":"Pelajari untuk mengetahui apa itu file APK dan API yang dapat membuat dan membuka file APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Apa itu file APK?

File dengan ekstensi .apk adalah file aplikasi Google Android yang digunakan untuk menginstal aplikasi (aplikasi) di perangkat Android. Itu dibuat sebagai file yang dapat dieksekusi menggunakan IDE resmi Google Android Studio, dan diunggah ke toko Google Play untuk diunduh dan diinstal oleh pengguna akhir. File APK dapat dibuat dan tersedia untuk instalasi manual juga sebelum dipublikasikan ke Google Play Store. Ini membantu dalam menguji fungsionalitas dan perilaku file paket APK yang dihasilkan. Oleh karena itu, perlu dipastikan bahwa file APK berasal dari sumber tepercaya dan tidak mengandung malware.

## Format File APK

File APK dikemas sebagai terkompresi dalam format file [ZIP](/id/compression/zip/) yang dapat dibuka dengan perangkat lunak pembuka file ZIP apa pun. Ekstensi .apk dari file semacam itu dapat diubah namanya menjadi .zip dan membuka file tersebut di aplikasi ZIP apa pun atau mengekstrak isinya.

## Isi Paket APK

Satu file APK berisi semua file yang diperlukan untuk penginstalan dan eksekusinya. File APK, ketika diekstraksi dengan aplikasi ZIP, berisi file dan folder berikut.

* `META-INF/`: Direktori yang berisi file manifes, tanda tangan, dan daftar sumber daya dalam arsip
* `lib/`: Direktori berisi kode terkompilasi yang terkait dengan platform tertentu seperti armeabi-v7a, x86, arm64-v8a, dll.
* `res/`: Direktori berisi sumber daya yang tidak dikompilasi seperti gambar
* `assets/`: Direktori yang berisi aset aplikasi, yang dapat diambil oleh AssetManager.
* `androidManifest.xml`: Berisi nama, informasi versi, dan konten file APK
* `classes.dex`: Ini adalah kelas Java terkompilasi yang dapat dijalankan di mesin virtual Dalvik dan oleh Android Runtime
* `resources.arsc`: File sumber daya terkompilasi seperti string

## Bagaimana cara menginstal file APK di Perangkat Android?

Untuk menginstal file APK di perangkat Android Anda, langkah-langkah berikut dapat digunakan.

1. Unduh APK menggunakan browser web
2. Ketuk – Anda kemudian dapat melihatnya mengunduh di bilah atas perangkat Anda
3. Setelah diunduh, buka Unduhan, ketuk file APK, dan ketuk Ya saat diminta.

Mengikuti langkah-langkah ini akan memulai pemasangan aplikasi di perangkat Anda.

## Referensi

* [Format File APK](https://en.wikipedia.org/wiki/Android_application_package)

