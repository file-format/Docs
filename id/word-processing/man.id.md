{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manual Unix",
  "description":"Pelajari tentang format file FODT dan API yang dapat membuat dan membuka file MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Apa itu file MAN?

File dengan ekstensi .man adalah singkatan dari halaman manual yang merupakan manual pengguna pemrograman Unix dalam bentuk dokumentasi perangkat lunak. Ini digunakan oleh utilitas `Man`, termasuk dalam Unix, yang digunakan untuk melihat dokumentasi. Dokumentasi perangkat lunak berisi informasi dalam bagian dan halaman yang dapat diambil menggunakan utilitas Man dari terminal perintah dengan mengeluarkan perintah. Tersedia di komputer sebagai soft copy dokumentasi, tidak memerlukan salinan cetak atau koneksi internet untuk mengaksesnya.

## Format File Man Manual Unix - Informasi Lebih Lanjut

Halaman manual disimpan dalam format teks biasa dan dapat dibuat dan dibuka di editor teks apa pun untuk dilihat atau diedit. Di UNIX, informasi dari halaman Man diambil dengan mengeluarkan perintah dari terminal yang menyertakan referensi ke bagian dan nomor halaman dari manual.

### Bagian dan Halaman

Unix man adalah manual sistem di mana setiap argumen halaman ke perintah mengacu pada nama program, utilitas, atau fungsi. perintah, jika dilengkapi dengan informasi bagian, akan mencari halaman di bagian tertentu itu. Namun, perilaku default adalah mencari halaman di semua bagian dan menampilkan halaman pertama terlepas dari apakah ada di beberapa bagian.

### Nomor Bagian

Berikut adalah informasi tentang nomor bagian dari manual diikuti dengan jenis halaman yang dikandungnya.

|Nomor Bagian|Jenis halaman|
---|---|
|1|Program yang dapat dijalankan atau perintah shell|
|2|Pemanggilan sistem (fungsi yang disediakan oleh kernel)|
|3|Pemanggilan pustaka (fungsi dalam pustaka program)|
|4|Berkas khusus (biasanya ditemukan di /dev)|
|5|Format dan konvensi file, misalnya /etc/passwd|
|6|Game|
|7|Lain-lain (termasuk paket dan konvensi makro), misalnya man(7), groff(7)|
|8|Perintah administrasi sistem (biasanya hanya untuk root)|
|9|Rutinitas kernel [Tidak standar]|

## Contoh - Bagaimana Cara Membaca Halaman MAN?

Berikut adalah contoh cara mengambil informasi tentang perintah MkDir menggunakan perintah Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Referensi

* [Spesifikasi Teknis OpenDocument - Oleh Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — halaman manual Linux](https://man7.org/linux/man-pages/man1/man.1.html)

