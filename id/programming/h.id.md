{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "apa itu file ah", "cara membuka file h", "ekstensi", "file", "file h", "format file h", "ekstensi file h", "Contoh Berkas H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas Tajuk H - C/C++",
  "description":"Pelajari tentang format file H dan API yang dapat membuat dan membuka file H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Apa itu file H?

File yang disimpan dengan **ekstensi file h** adalah file header yang digunakan dalam file C/C++ untuk menyertakan deklarasi variabel, konstanta, dan fungsi. Ini dirujuk oleh file implementasi [C++](/id/programming/cpp/) yang berisi implementasi sebenarnya dari fungsi-fungsi ini. File header .h juga dapat menyertakan informasi tambahan seperti definisi Makro. File header ini direferensikan dalam file C/C++ menggunakan direktif `#include`.

Proyek C++ baru biasanya berisi file header khusus dengan nama file **stdafx.h** yang merupakan titik awal untuk semua rantai kompilasi dan semua file header dapat disertakan dalam file tunggal ini. File .h dapat dibuka dengan editor teks apa saja, Eclipse IDE, Microsoft Visual Studio IDE, kompiler Borland C++ dan banyak aplikasi lainnya.

## Format File .H

File .h adalah file teks biasa yang memiliki aturan sendiri untuk menentukan sintaks. File header dapat berisi informasi berikut.

**`Variabel`** - Dalam kasus Pemrograman Berorientasi Objek (OOP), file header kelas berisi definisi semua variabel tingkat kelas yang dapat diakses di seluruh file kode sumber implementasi
**`Deklarasi Metode`** - Semua deklarasi metode disertakan dalam file header .h agar dapat diakses di beberapa file implementasi.
**`Non-Inline Function Definitions`** - File header juga dapat berisi definisi metode non-inline.
**`Message Maps`** - File header juga dapat berisi peta pesan jika implementasi kode sumber MFC. Dalam kasus seperti itu, peta pesan ditautkan ke implementasi fungsionalitas yang ditautkan ke elemen UI seperti tombol, kotak centang, tombol radio, dll.


### Pengawal Tajuk

File header dapat menimbulkan kesalahan kompleks di mana banyak deklarasi disertakan dalam file yang sama sebagai hasil dari penambahan file header lainnya. Definisi duplikat ini menimbulkan kesalahan kompiler. Situasi bermasalah ini dapat dihindari melalui mekanisme yang disebut header guard yang merupakan arahan kompilasi bersyarat seperti yang ditunjukkan di bawah ini.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Dengan header ini, preprosesor memeriksa apakah `ANY_UNIQUE_NAME_HERE` telah ditentukan. Jika header berulang kali dimasukkan ke dalam file yang sama, isi header akan diabaikan.

## Contoh File H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Referensi

* [Filer Header - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

