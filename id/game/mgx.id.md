{
  "date" : "2021-09-08",
  "keywords" :[ "file mgx", "format file mgx", "apa itu file mgx", "file", "contoh mgx", "ekstensi file mgx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file MGX Expansion Replay Age of Empires 2 dan API yang dapat membuat dan membuka file MGX.",
  "title" :"MGX - Pemutaran Ulang Ekspansi Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Apa itu file MGX?

File dengan ekstensi .mgx adalah file rekaman untuk game Age of Empires II: The Conquerors yang dapat diputar ulang dalam program Age of Empires II. Ini berisi rekaman lengkap dari kampanye yang dimainkan oleh pengguna. Itu dapat dimuat dan diputar ulang di dalam program Age of Empires II. Setelah diputar ulang, game tersebut menampilkan semua peristiwa dan skenario yang direncanakan pengguna untuk kampanye dan dimainkan.

## Format File MGX - Informasi Lebih Lanjut

Format file internal file MGX telah dikerjakan dan tersedia sebagai informasi yang divalidasi sebagian di [Age of Empires 2: The Conquerors — Spesifikasi Format File Savegame](https://github.com/stefan-kolb/aoc-mgx-format). Spesifikasi menguraikan rincian di bagian berikut.

### Definisi Struktur

Definisi struktur format file GPX diyakini didasarkan pada [deklarasi BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) yang menyediakan cara untuk membaca dan menulis data biner terstruktur. Ini memungkinkan pemrogram menentukan format data biner yang kemudian dibaca dan ditulis oleh BinData.

### Pesan MGX

Olahpesan MGX didasarkan pada dua jenis pesan.

* GAMESTART - menentukan perintah mulai game dan belum divalidasi hingga saat ini
* CHAT - menjelaskan pesan obrolan dalam game. Baik pemain maupun game itu sendiri (Gaia) dapat memancarkan pesan dalam game.

### TINDAKAN GAMEPLAY

Ada beberapa [Tindakan GAMEPLAY](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) yang telah diambil dan detailnya tersedia.

## Referensi

* [Age of Empires 2: The Conquerors — Spesifikasi Format File Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

