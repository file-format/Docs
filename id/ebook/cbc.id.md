{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "ekstensi", "file", "format", "Buku komik", "Format File Buku Komik", "eBuku" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file CBC dan API yang dapat membuat dan membuka file CBC.",
  "title" :"CBC - Format File Koleksi Buku Komik",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Apa itu file CBC?

File dengan ekstensi .cbc adalah kumpulan file Buku Komik terkompresi untuk eBook dan berisi file [CBZ](/id/ebook/cbz/) dan [CBR](/id/ebook/cbr/). Ini digunakan oleh [Calibre](https://calibre-ebook.com/), sebuah aplikasi konversi eBook, yang merupakan pengelola e-book sumber terbuka lintas platform dan memungkinkan Anda mengelola eBook dan mengonversinya ke format yang berbeda . File CBC berisi file .txt, comics.txt, yang mencantumkan file lain yang merupakan bagian dari arsip. Beberapa aplikasi tersedia online yang dapat mengonversi file CBC ke [AZW3](/id/ebook/azw3/), [EPUB](/id/ebook/epub/), [FB2](/id/ebook/fb2/), [MOBI](/id/ebook/mobi/), [TXT](/id/word-processing/txt/), [PDF](/id/pdf/), dan format file populer lainnya.

## Format File CBC

File CBC adalah arsip terkompresi yang berisi CBZ, CBR, dan file teks untuk mencantumkan konten. File teks, comics.txt dikodekan UTF8 dan berisi daftar file CBC yang akan digunakan oleh pembaca untuk mengatur koleksi mereka. File CBC biasanya memiliki beberapa atribut yang memungkinkan pengaturan koleksi ini seperti Komik, Kategori, Penerbit, Seri, Edisi, dan Artis.

Isi file CBC sampel terdaftar sebagai berikut:

* comics.txt - File teks yang berisi daftar file CBR dan CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* File CBZ

di mana file comics.txt mencantumkan konten sebagai berikut:

* 1.cbz: Bab Pertama
* 2.cbz: Bab Kedua
* 3.cbz: Bab Ketiga

Pembaca memproses file comics.txt dan membuat daftar isi berdasarkan data yang disediakan.

## Referensi

* [Kaliber](https://calibre-ebook.com/)

