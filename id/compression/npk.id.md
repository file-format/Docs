{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File NPK",
  "description":"Pelajari tentang format file NPK dan API yang dapat membuat dan membuka file NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Apa itu file NPK?

File NPK adalah file paket pemutakhiran perangkat lunak yang digunakan oleh router **MikroTik** untuk pemutakhiran sistem operasi router. Itu datang sebagai arsip biner terkompresi yang dimuat di router untuk menginstal pembaruan perangkat lunak. Informasi yang terkandung di dalam file NPK termasuk informasi jaringan seperti alamat IP dan layanan IP, informasi konektor (antarmuka ethernet dan port serial), pengaturan email, konfigurasi jembatan, dan manajemen pengguna lokal.

## Format File NPK

File NPK disimpan sebagai arsip biner terkompresi. Ini adalah format file tertutup yang hanya digunakan oleh MikroTik sendiri. Itu tidak dimaksudkan untuk membuat add-on RouterOS melalui pihak ke-3. File NPK dikelola oleh MikroTik sendiri dan versi yang ditingkatkan dapat diunduh dari bagian unduhan situs web [MikroTik](https://mikrotik.com/download).

Saat file NPK diunggah ke router, OS router tidak akan berfungsi kecuali jika di-boot ulang. Oleh karena itu, diperlukan restart agar OS router dapat ditingkatkan.

## Referensi

* [MikroTik - Upgrade OS Router](https://mikrotik.com/download)
* [Cara Membuat File NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

