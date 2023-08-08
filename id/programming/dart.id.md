---
date: 2019-10-11
keywords: dart, .dart, format file dart, file dart, cara menjalankan file dart, ekstensi .dart
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File Dart
linktitle: Dart
description: "Pelajari tentang format file Dart dan API yang dapat membuat dan membuka file Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Apa itu file Dart? ##

File Dart berisi kode sumber bahasa pemrograman Dart yang merupakan bahasa pemrograman yang dioptimalkan untuk klien yang dikembangkan oleh Google yang digunakan untuk membangun aplikasi untuk seluler, desktop, web, IoT (Internet of things), dll. Dart adalah bahasa berorientasi objek dengan sintaks yang mirip dengan C. Dart dapat dikompilasi ke JavaScript atau kode asli. Anda dapat menjalankan file Dart di browser web terkenal seperti Anda dapat menjalankan file javascript. Alat baris perintah yang dikenal sebagai mesin virtual Dart yang disertakan dengan Dart SDK juga dapat digunakan untuk mengompilasi dan menjalankan file Dart.

## Sejarah Singkat ##

Proyek Dart didirikan oleh Lars Bak dan Kasper Lund dan versi pertama dirilis pada 14 November 2013. Pada awalnya Dart dikritik karena fragmentasi web karena rencana untuk menyertakan Dart VM di Google Chrome. Rencana tersebut dibatalkan dan Dart berfokus pada kompilasi ke JavaScript dengan rilis versi 1.9 pada tahun 2015.

Dart 2.0 dirilis pada Agustus 2018 di mana ekstensi dart2native diperkenalkan yang mengkompilasi kode Dart ke platform Linux, Windows, macOS asli. Ekstensi ini mengaktifkan executable mandiri karena SDK Dart tidak diperlukan untuk menjalankan aplikasi Dart dari platform tersebut. Ekstensi ini juga terintegrasi dengan Flutter sehingga memungkinkan untuk membuat aplikasi lintas platform.

Dart standar ECMA dengan edisi pertama pada Juli 2014 dan edisi kedua pada Desember 2014.


## Cara menjalankan/mengeksekusi kode Dart ##

Kode Dart dapat berjalan dengan cara berikut:

- **Dikompilasi sebagai JavaScript**:</br> Kode Dart dikompilasi ke JavaScript dengan menggunakan kompiler dart2js. Kode JavaScript yang dikompilasi kompatibel dengan semua browser web utama.
- **Berdiri sendiri**:</br> Kit Pengembangan Perangkat Lunak Dart (SDK) disertakan dengan Dart VM mandiri yang memungkinkan kode Dart dijalankan di antarmuka baris perintah. Dart dilengkapi dengan pustaka standar lengkap yang memungkinkan pengguna menulis aplikasi yang berfungsi penuh.
- **Ahead-of-time (AOT) dikompilasi**:</br> Kode Dart dapat dikompilasi AOT ke kode mesin yang memungkinkan aplikasi seluler dibuat dengan Flutter.
- **Warga asli**:</br> Dengan kompiler dart2native, kode Dart dapat dikompilasi menjadi executable mandiri yang dapat berjalan di Windows, Linux, dan macOS.

## Format File Panah ##

Dart adalah bahasa berorientasi objek gaya-C yang mendukung antarmuka, mixin, kelas abstrak, generik reified, dan antarmuka tipe.

### Sintaks ###

Berikut ini adalah beberapa contoh sintaks Dart.

#### Cetak ke Konsol ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Loop dan Array ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### Fungsi ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Kelas ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### Campuran ####

Mixin adalah kelas normal tempat kita dapat meminjam metode/variabel tanpa mewarisinya. Ini dilakukan dengan menggunakan kata kunci *"with"*.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## Referensi ##

- [Dart (bahasa pemrograman) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

