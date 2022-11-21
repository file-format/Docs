{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "apa itu file ac", "cara membuka file c", "ekstensi", "file", "file c", "format file c", "ekstensi file c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File Pemrograman Bahasa C - C",
  "description":"Pelajari tentang format file C dan API yang dapat membuat dan membuka file C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Apa itu file C?

File yang disimpan dengan ekstensi file c adalah file kode sumber yang ditulis dalam bahasa pemrograman C. **File C** mencakup semua implementasi fungsionalitas aplikasi dalam bentuk kode sumber. Deklarasi kode sumber ditulis dalam file header yang disimpan dengan ekstensi [.h](/id/programming/h/). C ++ adalah bentuk modern dari bahasa C dan digunakan untuk mengembangkan sebagian besar perangkat lunak saat ini.

## Sejarah Singkat

Bahasa C muncul sebagai hasil dari pembuatan berbagai utilitas untuk sistem operasi UNIX. Denis Ritchie, orang di balik pembuatan bahasa pemrograman ini, pekerjaan awalnya dimulai pada 1960-an dan awal 1970-an.

## Format File C

File C ditulis dalam format file teks biasa mengikuti sintaks bahasa pemrograman. File C tipikal akan memiliki:

* pernyataan impor di bagian atas file untuk mengimpor File header apa pun
* satu atau lebih metode untuk mengimplementasikan fungsionalitas yang diinginkan

### Impor Header

File header, dengan ekstensi .h, berisi pernyataan sertakan yang diperlukan untuk menyertakan file fungsionalitas lain dalam proyek. Selain itu, ini berisi deklarasi metode yang ditentukan dalam file implementasi. File header disertakan menggunakan pernyataan sertakan seperti yang ditunjukkan di bawah ini.

```
#include <filename.h>
```

### Implementasi Kode Sumber

Implementasi sebenarnya dari persyaratan fungsional dikodekan sebagai metode dalam file C. Setiap metode dalam file C memiliki tipe pengembalian, nama metode, dan mungkin memiliki beberapa parameter input. Jika tipe pengembalian tidak batal, metode mungkin mengembalikan beberapa nilai.

### Contoh Kode C
Berikut adalah contoh program ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referensi** ##

* [Penerapan Kelas - Oleh Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

