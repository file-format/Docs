---
date: 2019-10-11
keywords: java, .java, format file java, cara membuka file java, cara menjalankan file java, file java, contoh kode java
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File Jawa
linktitle: Java
description: "Pelajari tentang format file Java dan API yang dapat membuat dan membuka file Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Apa itu file Java? ##
File yang berisi kode sumber Java dan disimpan dengan ekstensi file .java dikenal sebagai file Java. Java adalah salah satu teknologi yang paling banyak digunakan untuk pengembangan aplikasi game, seluler, web, dan desktop. Karena Java adalah platform independen, ia bekerja dengan sempurna di Windows, Mac, Linux, Raspberry Pi, dll. Java sangat mirip dengan C# dan C++ sehingga lebih mudah untuk beralih di antara bahasa-bahasa tersebut.

## Sejarah Singkat ##

Proyek Java dimulai pada Juni 1991 oleh James Gosling, Mike Sheridan, dan Patrick Naughton. Java awalnya bernama Oak. Itu kemudian berganti nama menjadi Green dan akhirnya menjadi Java. James Gosling merancang Java dengan sintaks yang mirip dengan C/C++. Versi publik pertama Java dirilis pada tahun 1996 oleh Sun Microsystems. Itu bisa berjalan di semua sistem populer yang menyebabkan Java menjadi populer dengan cepat. Dengan dirilisnya Java 2 pada Desember 1998, beberapa konfigurasi untuk berbagai jenis platform dibangun. Versinya adalah sebagai berikut

- J2EE (Java EE): Untuk solusi perusahaan
- J2ME (Java ME): Untuk aplikasi seluler
- J2SE (Java SE): Untuk aplikasi desktop

Pada tanggal 19 November 2006, Java Virtual Machine (JVM) dirilis oleh Sun sebagai perangkat lunak bebas dan sumber terbuka. Setelah Oracle Corporation mengakuisisi Sun Microsystems pada 2009–2010, James Gosling mengundurkan diri dari Oracle pada 2 April 2010.

## Cara menjalankan/mengeksekusi kode Java ##

Untuk mengeksekusi kode Java, perlu dikompilasi terlebih dahulu. Untuk itu, diperlukan Java SDK. Java SDK mengkompilasi kode Java ke file kelas bytecode. Ada IDE seperti Eclipse dan IntelliJ Idea yang memudahkan bekerja dengan file Java dengan menyediakan penyelesaian kode dan antarmuka yang mudah digunakan untuk mengkompilasi dan mengeksekusi kode Java.

## Format File Java ##

Sintaks Java sangat dipengaruhi oleh C dan C++ tetapi tidak seperti C++, Java dibangun hampir secara eksklusif sebagai bahasa berorientasi objek. Di Java, semua kode ditulis di dalam kelas dan setiap item data adalah objek. Berbeda dengan C++, Java tidak mendukung operator overloading atau pewarisan berganda.

### kode sampel Java ###

Berikut ini adalah contoh sintaks Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Pada kode di atas, kata kunci **public** menunjukkan pengubah akses. Ini menyatakan bahwa kelas ini dapat diakses oleh kelas di luar hierarki kelas. Pengubah akses juga bisa **dilindungi** (dapat diakses dalam paket yang sama) atau **private** (metode hanya dapat diakses oleh kelas yang sama). **Statis** di depan metode menunjukkan bahwa metode dapat dipanggil tanpa instance kelas tertentu. **Void** menunjukkan bahwa metode tidak akan mengembalikan apa pun. Untuk mencetak string ke konsol. Perintah System.out.println digunakan. Dalam perintah ini, kelas *System* memiliki kolom statis *out* yang merupakan turunan dari kelas *PrintStream* yang berisi metode *println*.

Nama file dari file Java harus sama dengan nama kelas. Jadi file Java untuk kode contoh akan diberi nama *ExampleApp.java*.

## Referensi ##

- [Java (bahasa pemrograman) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

