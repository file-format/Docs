
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADS - Format File Spesifikasi Ada",
  "description":"Pelajari tentang apa itu format file ADS dengan contoh dan API yang dapat membuat dan membuka file ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Apa itu file ADS?

File ADS adalah file spesifikasi untuk proyek pemrograman Ada. Ini mirip dengan kelas untuk Java, atau pasangan header dan implementasi dalam kasus C++. Spesifikasi umum dan pribadi dari paket Ada disimpan dalam file .ads. Sebaliknya, file .adb berisi implementasi, atau badan Ada. Seperti [C++](/id/programming/cpp/), Ada menawarkan pemisahan antara spesifikasi dan implementasi yang tidak bergantung pada OOP.

File ADS dapat dibuka di editor teks apa pun seperti Microsoft Notepad, Notepad ++, dan Atom.

## Format File ADS

File ADS dalam format file teks biasa sederhana dan dapat dibuka/diedit dengan editor teks apa pun. Ada paket dapat diatur ke dalam hierarki. Unit anak dapat dideklarasikan dengan cara berikut:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Referensi

* [Paket Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

