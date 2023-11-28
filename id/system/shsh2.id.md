{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File SHSH2 - Format File Gumpalan SHSH iOS",
  "description":"Pelajari tentang apa itu file SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Apa itu file SHSH2?

File SHSH2, juga dikenal sebagai blob SHSH atau ECID SHSH, adalah tanda tangan digital yang digunakan oleh Apple untuk mengautentikasi dan memverifikasi pembaruan firmware untuk perangkat iOS seperti iPhone, iPad, dan iPod. Ini berisi pengidentifikasi unik untuk perangkat yang dikenal sebagai ECID (Exclusive Chip ID). Ini juga berisi informasi tentang versi firmware yang diinstal pada perangkat.

## Format File SHSH2 - Informasi Lebih Lanjut

File SHSH2 disimpan ke disk dalam format file biner dan detail struktur file internal format file ini tidak tersedia untuk umum.

Saat iOS versi baru diinstal di perangkat Apple seperti iPhone, iPad, atau Mac, file SHSH2 akan dibuat. File SHSH2 ini dikirim ke server Apple yang membaca dan memverifikasi file tanda tangan digital ini. Berdasarkan informasi ini, server mengizinkan atau mencegah instalasi.

Hal yang sama terjadi ketika pembaruan diminta. Saat pengguna meminta pembaruan atau pemulihan perangkat mereka melalui iTunes atau perangkat lunak lain, server Apple akan memeriksa apakah file SHSH2 cocok dengan ECID dan versi firmware perangkat sebelum mengizinkan pembaruan untuk dilanjutkan.

## Referensi

* [Gumpalan SHSH - Oleh Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Penghemat TSS](https://tsssaver.1conan.com/v2/)

