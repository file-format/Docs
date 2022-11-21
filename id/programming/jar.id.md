{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "apa itu file jar", "cara membuka file jar", "ekstensi", "file", "file jar", "format file jar", "ekstensi .jar " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Format File Arsip Java",
  "description":"Pelajari tentang format file JAR dan API yang dapat membuat dan membuka file JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file JAR?

File dengan ekstensi .jar adalah file Arsip Java yang berisi banyak file terkait aplikasi yang berbeda sebagai satu file. Format file ini dibuat untuk mengurangi kecepatan memuat Java Applet yang diunduh di browser melalui transaksi HTTP, dengan menghindari pembuatan banyak koneksi HTTP. File JAR tunggal dapat berisi file kelas Java ([.class](/id/programming/class/)), [images](/id/image/), dan [sounds](/id/audio/). Item individual di dalam file JAR dapat ditandatangani secara digital oleh pengembang aplikasi untuk mengautentikasi asalnya. File JAR secara teratur digunakan untuk membuat API fungsional yang berisi fungsionalitas khusus yang terkait dengan API tersebut.

## Format File .JAR

File JAR didasarkan pada [format file ZIP](/id/compression/zip/) populer yang mengarsipkan file konten individualnya dalam satu file. Format file JAR mendukung kompresi, menghasilkan ukuran file yang lebih kecil untuk diunduh dan karenanya semakin meningkatkan waktu pengunduhan. Artikel [spesifikasi file JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) oleh Oracle memberikan detail lengkap tentang spesifikasi internal file JAR.

### Berkas Manifes

Saat file JAR dibuat, file manifes secara otomatis dibuat di dalamnya yang berisi informasi metadata tentang konten file JAR. File ini menampilkan konten yang dikemas di dalam file JAR. File Manifest tipikal terlihat sebagai berikut yang menunjukkan folder dan kelas yang disertakan dalam file JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Spesifikasi Manifes

Spesifikasi manifes didefinisikan oleh Oracle sebagai berikut.

`file manifes`: baris baru bagian utama \*bagian-individu

`bagian-utama`: info-versi baris baru \*atribut-utama

`version-info`: Manifest-Version : nomor-versi

`nomor versi` : digit+{.digit+}*

`main-attribute`: (semua atribut utama yang sah) baris baru

`individual-section`: Name : value newline \*perentry-attribute

`perentry-attribute`: (atribut perentry yang sah) baris baru

`baris baru` : CR LF | JIKA | CR (tidak diikuti oleh LF)

`digit`: {0-9}

### JAR yang dapat dijalankan

File JAR juga dapat terdiri dari aplikasi yang dapat dijalankan oleh Java Virtual Machine (JVM) yang mirip dengan aplikasi lain di Sistem Operasi Microsoft Windows. Dalam hal ini, JVM perlu mengetahui tentang titik masuk aplikasi yaitu kelas apa pun dengan metode utama public static void. File manifes mengidentifikasi kelas tersebut dengan header `Main-Class` dalam format berikut:

```
Main-Class: com.example.MyClassName
```



## Referensi

* [Ringkasan File JAR](https://docs.Oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Format File JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,ke%20one%20file%20for% 20distribution.&text=Mereka%20%20dibangun%20on%20the,jar%20file%20extension.)

