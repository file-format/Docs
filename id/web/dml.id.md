{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "file DML", "format file DML", "tipe file DML", "file", "tipe", "apa itu file DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - Berkas HTML DynaScript",
  "description":"Pelajari tentang format file DML dan API yang dapat membuat dan membuka file DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Apa itu file DML?

File dengan ekstensi .dml adalah file kode halaman skrip web yang dibuat dengan DyanScript. DynaScript adalah bahasa skrip [HTML](/id/web/html/) dinamis yang kompatibel dengan ECMAScript dan menyediakan sebagian besar fitur yang sama seperti bahasa skrip lainnya. Ini mirip dengan kode ColdFusion dan kode Microsoft Active Server Pages (ASP). File DML dapat dibuka dan dilihat di browser web standar yang mirip dengan halaman HTML lainnya.

## Format File DML

File DML dibuat dalam format file teks biasa dan dapat dibuka dengan editor teks untuk melihat kodenya. Penulisan kode menggunakan bahasa skrip DML dapat digunakan untuk menghasilkan HTML secara dinamis di halaman DML yang dihosting di sisi server. DynaScript dibangun dari elemen bahasa berikut:


* SCRIPT tag - Ini disematkan dalam dokumen sebagai komentar HTML. Komentar HTML ditandai dengan \ <!-- tag.
* Literal - Ini adalah nilai tetap dalam file DynaScript. Contohnya termasuk bilangan bulat seperti s 123 , 0x3F , 0123, bilangan titik-mengambang seperti 456.789 , 3.2e-8, Boolean seperti benar atau salah, dan string seperti "Hujan di Spanyol"
* Variabel - Variabel DynaScript tidak perlu didefinisikan atau ditetapkan ke tipe data tetap. Variabel harus memiliki nilai sebelum Anda menggunakannya dalam ekspresi; jika tidak, peringatan runtime dihasilkan.
* Ekspresi - Ini adalah kombinasi variabel, nilai literal, operator, dan ekspresi lainnya. Sisi kanan pernyataan penugasan adalah ekspresi.
* Operator - Ini beroperasi pada satu atau lebih ekspresi yang disebut operan. Ini bisa berupa ternary, binary atau unary: operator ternary bertindak atas tiga ekspresi, operator biner bertindak atas dua ekspresi, dan operator unary bertindak atas satu ekspresi.
* Pernyataan - Aliran skrip kontrol ini, memanipulasi objek, dan pemrograman umum. Secara umum, pernyataan ini mengikuti sintaks C dan Java standar. Contohnya adalah if-else, do-while loop, switch, break, continue, dll. seperti bahasa scripting lainnya.
* Fungsi - Fungsi, seperti bahasa skrip lainnya, memungkinkan Anda untuk mengenkapsulasi serangkaian instruksi sekali dalam dokumen sebagai fungsi, lalu menggunakannya beberapa kali di seluruh dokumen (dengan memanggil fungsi). DynaScript juga mendukung fungsi.
* Objek - DynaScript berorientasi objek dan mendukung `objek` dan konsep dasar berorientasi objek dari Enkapsulasi, Polimorfisme, dan Pewarisan.

