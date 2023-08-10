{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "format file", "apa itu file pak", "file", "contoh pak", "File Paket Video Game", "ekstensi"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang file .pak dan API yang dapat membuat dan membuka file PAK.",
  "title" :"Format File PAK- File Paket Video Game",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Apa itu file PAK?

File PAK adalah file paket yang dibuat oleh berbagai gim video untuk mengarsipkan data gim. Pada dasarnya, ini adalah format file game. Ini dapat mencakup beberapa elemen game seperti grafik, tekstur, suara, objek, bersama dengan data game lainnya. Arsip sebagian besar disimpan sebagai file .zip dan dapat diekstraksi dengan perangkat lunak dekompresi populer seperti WinZip dan WinRAR. Contoh video game yang menggunakan file PAK antara lain Quake, Hexen, Crysis, dan Half-Life.

## Format File PAK - Informasi Lebih Lanjut

Umumnya, file PAK disimpan dalam [format file ZIP](/id/compression/zip/). Tetapi aplikasi yang berbeda mungkin menggunakan format file yang berbeda untuk menyimpan file-file ini.


## Bagaimana cara membuka file PAK?

Anda dapat membuka file PAK dengan aplikasi seperti [PakExplorer](https://www.quaketerminus.com/tools.shtml) dan [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -------------------------**

## Format File PAK - File Objek Simutrans

File dengan ekstensi .pak adalah format file game simulasi transportasi [Simutrans](https://www.simutrans.com/en/). Ini berisi objek yang digunakan dalam simulasi seperti grafik buatan pengguna dan konten data. Itu dapat memiliki beberapa objek berbeda seperti kendaraan game, bangunan, medan, dll. File PAK dihasilkan menggunakan MakeObject, sebuah utilitas yang mengkompilasi file .dat dan gambar .png untuk membuat objek simulasi ini. Simutrans memungkinkan para pemain untuk menjalankan sistem transportasi yang sukses dengan membangun dan mengelola sistem transportasi untuk penumpang, surat, dan barang melalui darat

## Bagaimana Cara Membuat File PAK?

Simutrans telah mencantumkan contoh contoh untuk membuat file PAK di OS Windows dan Linux.

### OS Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### BE/OS Linux

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Referensi

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

