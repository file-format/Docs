{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PYC dan API yang dapat membuat dan membuka file PYC.",
  "title" :"Format File PYC- File yang Dikompilasi Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Apa itu file PYC?

File PYC adalah file keluaran terkompilasi yang dihasilkan dari kode sumber yang ditulis dalam bahasa pemrograman Python. Ketika file PY dijalankan menggunakan juru bahasa Python, itu diubah menjadi bytecode untuk dieksekusi. Pada saat yang sama, bytecode yang dikompilasi juga disimpan sebagai file .pyc untuk digunakan kembali dari cache di lain waktu jika berlaku.

## Struktur Format File PYC

File PYC dalam bytecode dan spesifikasi format filenya tidak tersedia untuk umum. Namun, penyelidikan oleh beberapa sumber menunjukkan bahwa [struktur file PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) terdiri dari:

* `Numbe`r ajaib empat byte - Cukup dua byte yang berubah dengan setiap perubahan pada kode marshalling, lalu dua byte 0d0a.
* `Stempel waktu modifikasi empat byte` - Stempel waktu modifikasi Unix dari file sumber yang menghasilkan .pyc, sehingga dapat dikompilasi ulang jika sumbernya berubah.
* `A marshalled code object` - output dari marshal.dump dari objek kode yang merupakan hasil dari kompilasi file sumber.

## Referensi

* [Struktur file .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

