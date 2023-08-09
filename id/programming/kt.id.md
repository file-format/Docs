---
date: 2019-10-11
keywords: kt, .kt, format file kotlin, cara membuka file kotlin, cara menjalankan file kotlin, format file .kt, file kt, ekstensi file kotlin, ekstensi .kt, kotlin vs java
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File KT
linktitle: KT
description: "Pelajari tentang format file KT dan API yang dapat membuat dan membuka file KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Apa itu file KT? ##

Kode sumber yang ditulis dalam Kotlin disimpan dengan ekstensi .kt yang umumnya dikenal sebagai **ekstensi file Kotlin**. Kotlin adalah bahasa pemrograman lintas platform tujuan umum yang dikembangkan oleh JetBrains agar dapat dioperasikan sepenuhnya dengan [Java](/id/programming/java/). Merek dagang Kotlin dilindungi oleh Kotlin Foundation.

Kotlin diumumkan sebagai bahasa pemrograman pilihan untuk pengembangan Aplikasi Android oleh Google pada 7 Mei 2019. Android Studio 3.0 mulai mendukung Kotlin sebagai alternatif untuk pengembangan Aplikasi Android pada Oktober 2017.

## Sejarah Singkat Format File Kotlin KT##

Kotlin diluncurkan oleh JetBrains pada Juli 2011 sebagai bahasa pemrograman baru untuk JVM. Pimpinan JetBrains Dmitry Jemerov mengatakan bahwa sebagian besar bahasa tidak memiliki fitur yang mereka cari kecuali Scala tetapi kompilasi Scala yang lambat merupakan kekurangannya. Salah satu tujuan utama Kotlin adalah mengkompilasi secepat Java. Proyek Kotlin bersumber terbuka di bawah Lisensi Apache 2 pada Februari 2012.

Kotlin versi 1.0 dirilis pada 15 Februari 2015. Android mengumumkan dukungan kelas satu untuk Kotlin di Android di Google I/O 2017. Kotlin 1.2 dirilis pada 28 November 2017 dengan kemampuan berbagi kode antara platform JVM dan JavaScript. Kotlin 1.3 dirilis pada 29 Oktober 2018 dengan dukungan untuk pemrograman asinkron. Google mengumumkan Kotlin sebagai bahasa pemrograman pilihan untuk pengembangan Aplikasi Android pada 7 Mei 2019. Kotlin 1.4 dirilis pada Agustus 2020 dengan beberapa perubahan kecil untuk mendukung interoperabilitas dengan Swift/Objective-C.

## Sintaks Kotlin ##

Kotlin dirancang untuk menjadi lebih baik dari Java tetapi tetap dapat dioperasikan dengan kode Java untuk memungkinkan migrasi bertahap dari Java ke Kotlin.

* Titik koma bersifat opsional di Kotlin. Baris baru cukup untuk menunjukkan akhir pernyataan.
* Kotlin mendukung dua jenis variabel, read-only, ditentukan oleh kata kunci *val*, dan dapat diubah, ditentukan oleh kata kunci *var*.
* Kelas bersifat pribadi dan final secara default. Untuk menurunkan dari sebuah kelas, kelas dasar harus dideklarasikan dengan kata kunci *buka*.
* Kotlin juga mendukung pemrograman prosedural.
* Titik masuk ke program Kotlin adalah fungsi "utama" yang mirip dengan Java, C#, dll.

### Contoh Sintaks ###

Berikut ini adalah contoh sintaks Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Pada kode di atas, kata kunci **fun** mendefinisikan fungsi bernama main. Di dalam fungsi, variabel read-only 'audience' dideklarasikan dengan kata kunci **val**. Dengan menggunakan metode **println**, "Hello World from Kotlin" dicetak di konsol. Nilai audiens variabel dimasukkan ke dalam string dengan tanda **$**.

## Kotlin vs Java
Kotlin adalah bahasa resmi untuk menulis aplikasi Android dengan menawarkan banyak fitur canggih, tetapi banyak pengembang ahli Java masih tidak menunjukkan minat untuk beralih ke Kotlin. Mereka berpikir bahwa mereka dapat melakukan semuanya hanya dengan Java. Berikut adalah perbandingan antara dua teknologi yang dapat meyakinkan para pengembang java untuk beralih:

| Parameter | Jawa | Kotlin |
|-----------------------|------------|---------------- -|
| Obyek lajang | √ | √ |
| Jenis Wildcard | √ | Χ |
| Kompilasi | Bytecode | Mesin Virtual |
| Ekspresi Lambda | Χ | √ |
| Larik Invarian | Χ | √ |
| Bidang Non-Pribadi | √ | Χ |
| Pemeran Cerdas | Χ | √ |
| Keselamatan Null | Χ | √ |
| Anggota Statis | √ | Χ |

## Referensi ##

- [Kotlin (bahasa pemrograman) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

