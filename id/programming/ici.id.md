{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "file", "ekstensi", "format file", "implementasi ICI", "Panduan Pemrograman", "contoh ici", "bahasa pemrograman ICI", "modul ICI", "model data ICI ", "dokumentasi ICI", "bahasa ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - File Bahasa Pemrograman",
  "description":"Pelajari tentang format file ICI dan API yang dapat membuat dan membuka file ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Apa itu file ICI?

Bahasa pemrograman tujuan umum yang ditafsirkan dan berisi beberapa fitur seperti pengetikan dinamis bersama dengan tipe data fleksibel dikenal sebagai bahasa pemrograman ICI (bukan akronim). Ini dianggap mirip dengan bahasa [Perl](/id/programming/pl/). Bahasa ICI ini terdiri dari konstruksi kontrol aliran dan juga berisi beberapa operator bahasa C. Ini bukan bahasa berorientasi objek tetapi beberapa fitur OOP dapat dicapai dengan metode pewarisan khusus yang dikenal sebagai superstruktur. Mirip dengan [C](/id/programming/c), bahasa pemrograman ICI ini memiliki antarmuka sistem yang sama dan pustaka standar untuk fungsi bawaan.


## Sejarah Singkat ##

Pada akhir 1980-an, ini dikembangkan oleh Tim Long sebagai bahasa pemrograman yang ditafsirkan untuk tujuan umum. Sebagian besar fitur bahasa ini mirip dengan C dan juga dapat mencapai beberapa fitur dengan menerapkan beberapa metode khusus. Bahasa ini dimiliki sebagai domain publik dan tersedia sebagai bahasa yang dapat dijual kembali dan tidak ada yang harus menyebutkan dari mana dia mendapatkan kode sumbernya. Dokumentasi ICI berada di bawah hak cipta Canon Information System Research Australia.

## Spesifikasi Teknis ##

Ada dua tipe data berbeda yang digunakan dalam bahasa ini. Keduanya adalah tipe data Primitif dan Agregat. Keduanya termasuk ekspresi yang berbeda sesuai dengan komposisi yang telah ditentukan sebelumnya dalam bahasa. Modul yang berbeda seperti nested dan subrutin didukung oleh bahasa ini. Karena beberapa propertinya mirip dengan Perl, ia memiliki integrasi yang ketat dengan ekspresi reguler.

Set dibatasi untuk menjadi heterogen dan bersarang. Set ini memberikan dukungan untuk operasi set yang umum digunakan seperti Union dan Intersection dll. Sebagian besar digunakan sebagai bahasa untuk implementasi inti untuk aplikasi yang dimiliki oleh organisasi multinasional.

Hampir semua jenis program dapat ditulis dalam bahasa ini dan sebagian besar program khusus yang melibatkan struktur data kompleks ditulis dalam bahasa pemrograman ICI. Aplikasi dapat melibatkan implementasi ICI dengan cara yang harus ditulis di dalamnya. Bagian fungsional dari aplikasi dapat diimplementasikan oleh modul ICI. Bahasa ICI agak mirip dengan bahasa C tetapi model data ICI cukup tinggi dan berbeda dengan tipe seperti kamus (struct), set, array dinamis, ekspresi reguler, dan string (nyata).


## Contoh Format File ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referensi ##

* [Bahasa Pemrograman ICI](http://atrn.org/ici/doc/ici.html)



