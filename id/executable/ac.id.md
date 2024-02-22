{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Pelajari tentang format file AC dan API yang dapat membuat dan membuka file ACCDB.",
  "title" : "Format File AC - File Skrip Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-id",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Apa itu file AC?

File AC adalah file skrip Autoconf. **Autoconf** adalah paket makro M4 yang dapat diperluas yang menghasilkan skrip shell untuk mengonfigurasi paket kode sumber perangkat lunak secara otomatis. Skrip ini dapat mengadaptasi paket ke berbagai jenis sistem mirip UNIX tanpa campur tangan pengguna secara manual. Autoconf membuat skrip konfigurasi untuk sebuah paket dari file templat yang mencantumkan fitur sistem operasi yang dapat digunakan paket tersebut, dalam bentuk panggilan makro M4.

Producing configuration scripts using Autoconf requires GNU M4. Anda harus menginstal GNU M4 (setidaknya versi 1.4.6, meskipun direkomendasikan 1.4.13 atau lebih baru) sebelum mengonfigurasi Autoconf, sehingga skrip konfigurasi Autoconf dapat menemukannya. Skrip konfigurasi yang dihasilkan oleh Autoconf bersifat mandiri, sehingga penggunanya tidak perlu memiliki Autoconf (atau GNU M4).

## Bagaimana cara membuka file AC?

AC adalah singkatan dari Konfigurasi Otomatis. Ini adalah skrip yang dihasilkan oleh GNU Autoconf yang memungkinkan kode sumber perangkat lunak diadaptasi ke berbagai sistem mirip Posix dengan menguji fitur-fitur yang diperlukan dalam paket. Skrip ini disebut file AC.

## Komponen Autotools Utama

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools adalah kumpulan paket terkait yang, bila digunakan bersama-sama, menghilangkan banyak kesulitan dalam membuat perangkat lunak portabel. Alat-alat ini, bersama dengan beberapa file input upstream yang relatif sederhana, digunakan untuk membuat sistem build untuk sebuah paket.

**Ringkasan dasar tentang bagaimana komponen autotools utama cocok satu sama lain.**

!{{HIPERLINK1}}

Dalam pengaturan sederhana:

- Program `autoconf` menghasilkan skrip konfigurasi dari `configure.in` atau `configure.ac`.
- Program `automake` menghasilkan Makefile.in dari Makefile.am.
- Skrip `configure` dijalankan untuk menghasilkan satu atau lebih file Makefile dari file Makefile.in.
- Program `make` menggunakan Makefile untuk mengkompilasi program.

## Referensi
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Dasar-dasar Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



