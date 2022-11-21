{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "file", "ekstensi", "format file", "C++", "Bahasa Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - File Kode Sumber C++",
  "description":"Pelajari tentang format file CPP dan API yang dapat membuat dan membuka file CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file C++?

File dengan ekstensi file CPP adalah file kode sumber untuk aplikasi yang ditulis dalam bahasa pemrograman C++. Satu proyek C++ dapat berisi lebih dari satu file CPP sebagai kode sumber aplikasi. Proyek semacam itu terdiri dari berbagai jenis file, di mana file CPP dikenal sebagai file implementasi karena berisi semua definisi metode yang dideklarasikan dalam file header (.h). Proyek C++ secara keseluruhan menghasilkan aplikasi yang dapat dieksekusi saat dikompilasi secara keseluruhan.

## Struktur File CPP

Struktur file CPP sederhana dibandingkan dengan file header. Tujuan utama dari file implementasi semacam itu adalah untuk memisahkan antarmuka dari implementasi. Ini menghasilkan deklarasi semua fungsi anggota di file header dan detailnya di dalam file CPP. File implementasi CPP dapat digunakan sebagai file sederhana untuk menulis aplikasi atau sebagai implementasi kelas.

### Implementasi Independen

File CPP ketika digunakan sebagai aplikasi independen dapat berisi semua implementasi di dalamnya tanpa persyaratan deklarasi metode di file header. Implementasi seperti itu terdiri dari semua metode yang didefinisikan dalam file implementasi di mana masuknya aplikasi diatur oleh metode utama yang menggunakan input pengguna opsional sebagai argumen. Itu juga dapat menyertakan pustaka apa pun dari Pustaka Standar C++ untuk digunakan oleh metode apa pun yang dideklarasikan dalam file.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Implementasi Kelas

Dalam Pemrograman Berorientasi Objek (OOP), file CPP digunakan sebagai definisi kelas. Dalam kasus seperti itu, semua anggota data kelas dan fungsi anggota dideklarasikan di dalam file header. Setiap file header pada gilirannya dapat memiliki referensi ke metode perpustakaan standar juga. File CPP definisi kelas merujuk ke file header dalam pernyataan sertakan di awal file. Sebagian besar, pengembang perangkat lunak menyertakan komentar di awal file implementasi kelas seperti itu yang memberikan informasi tentang konten file yang sebenarnya, detail penulis, dan tanggal implementasi. Dalam kasus seperti itu, file implementasi header harus memiliki nama yang sama. Contoh dari file header dan implementasi tersebut adalah sebagai berikut.

### Berkas Tajuk

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### File Implementasi CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referensi

* [Penerapan Kelas - Oleh Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

