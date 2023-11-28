
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ke-4 - Format File Bahasa Keempat",
  "description":"Pelajari tentang format file .4 dengan contoh dan API yang dapat membuat dan membuka file ke-4.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Apa itu file ke-4?

File dengan ekstensi file .4 adalah file pemrograman yang dibuat untuk **Bahasa Pemrograman Keempat**. Ini berisi kode sumber untuk program yang ditulis dalam bahasa pemrograman Forth dan menghasilkan output ketika program dijalankan. Ini hanyalah file bahasa pemrograman lain yang mirip dengan file sumber [C](/id/programming/c/) dan [C++](/id/programming/cpp/).

## Format File ke-4 - Informasi Lebih Lanjut


### Contoh Kode Bahasa Pemrograman ke-4

Berikut adalah contoh program sederhana yang ditulis dalam Forth yang menghitung faktorial suatu bilangan:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Dalam contoh ini, kata faktorial mengambil satu argumen n dan mengembalikan faktorialnya. Kata dup menduplikasi nilai di atas tumpukan, drop membuang nilai di atas tumpukan, dan * mengalikan dua nilai di atas tumpukan. Konstruksi if dan Begin/Until mengontrol aliran program.

Untuk menggunakan program ini, Anda perlu memasukkan definisi ke dalam interpreter Forth, lalu memanggil kata faktorial dengan bilangan yang ingin Anda cari faktorialnya:

```
10 factorial .
```
Ini akan menghasilkan keluaran 3628800, yang merupakan faktorial dari 10.

## Referensi

* [Bahasa Pemrograman Keempat](https://en.wikipedia.org/wiki/Forth_(bahasa_pemrograman))

