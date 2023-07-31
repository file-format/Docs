{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "apa itu file .hh", "cara membuka file .hh", "ekstensi", "file", "file .hh", "format file .hh", " ekstensi file .hh","Contoh File .HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas Tajuk HH - C++",
  "description":"Pelajari tentang format file HH dan API yang dapat membuat dan membuka file HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Apa itu file HH?

File dengan ekstensi .hh adalah file header C++ yang menyertakan deklarasi variabel, konstanta, dan fungsi. Deklarasi ini digunakan oleh file implementasi C++ yang sesuai, biasanya disimpan sebagai file [.cpp](/id/programming/cpp/) yang berisi implementasi sebenarnya dari logika pengguna. File header .hh direferensikan dalam file implementasi CPP menggunakan direktif `#include`. Anda dapat menambahkan sebanyak mungkin file header ke proyek C++ untuk menyertakan deklarasi tingkat proyek.

## Format File .HH

File .hh adalah file teks biasa yang dibuat dengan tetap memperhatikan aturan definisi file header. Informasi paling umum yang dideklarasikan dalam file .hh meliputi yang berikut ini.

**`Variabel`** - Dalam kasus Pemrograman Berorientasi Objek (OOP), file header kelas berisi definisi semua variabel tingkat kelas yang dapat diakses di seluruh file kode sumber implementasi
**`Deklarasi Metode`** - Semua deklarasi metode disertakan dalam file header .h agar dapat diakses di beberapa file implementasi.
**`Non-Inline Function Definitions`** - File header juga dapat berisi definisi metode non-inline.
**`Message Maps`** - File header juga dapat berisi peta pesan jika implementasi kode sumber MFC. Dalam kasus seperti itu, peta pesan ditautkan ke implementasi fungsionalitas yang ditautkan ke elemen UI seperti tombol, kotak centang, tombol radio, dll.

## Perbedaan Antara File .H dan .HH

Tampaknya, tidak ada perbedaan antara file header .h dan .hh selain dari cara penggunaan yang disarankan untuk masing-masing bahasa yaitu [C](/id/programming/c/) atau C++. Memberi nama file header Anda sesuai dengan bahasa ini membantu Anda membedakannya dalam proyek besar yang dapat berupa campuran implementasi C dan C++.

Selain itu, jika header dipisahkan oleh ekstensi, editor Anda dapat menerapkan pemformatan yang sesuai secara otomatis untuk masing-masingnya.

Secara keseluruhan, perbedaan kedua format file ini tidak akan merugikan, tetapi akan menguntungkan, dan dianjurkan untuk mengikuti perbedaan C dan C++.

### Pengawal Tajuk

File header dapat menimbulkan kesalahan kompleks di mana banyak deklarasi disertakan dalam file yang sama sebagai hasil dari penambahan file header lainnya. Definisi duplikat ini menimbulkan kesalahan kompiler. Situasi bermasalah ini dapat dihindari melalui mekanisme yang disebut header guard yang merupakan arahan kompilasi bersyarat seperti yang ditunjukkan di bawah ini.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Dengan header ini, preprosesor memeriksa apakah `ANY_UNIQUE_NAME_HERE_HPP` telah ditentukan. Jika header berulang kali dimasukkan ke dalam file yang sama, isi header akan diabaikan.

## Referensi

* [Filer Header - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Perbedaan antara format file .h dan .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

