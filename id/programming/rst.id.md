{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File RST- File Teks Berstruktur Ulang",
  "description":"Pelajari tentang format file RST dan API yang dapat membuat dan membuka file RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Apa itu file RST?

File RST adalah format file dokumentasi teknis, yang digunakan terutama di komunitas pemrograman Python. Ini adalah file teks yang ditulis dalam bahasa markup reStructuredText yang menerapkan gaya dan pemformatan ke dokumen teks biasa untuk pembuatan dokumentasi. File RST menggunakan komentar dan informasi lain dalam kode program Python untuk membuat dokumentasi teknis aplikasi. Namun, ini juga dapat berisi teks yang dapat diubah menjadi halaman web sederhana dan [eBuku](/id/ebook/). Editor teks seperti Github Atom, GNU Emacs (lintas platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) dan Vim (Linux) dapat digunakan untuk membuka file RST.

## Format File RST

File RST berisi kode yang ditulis dalam bahasa markup reStructuredText. Ini adalah bagian dari proyek Docutils dari Python Doc-SIG (Documentation Special Interest Group) yang menyediakan seperangkat alat untuk Python mirip dengan Javadoc untuk Java. Parser untuk format file RST disematkan di Docutils dan dapat mengekstrak informasi dari program Python untuk memformatnya ke dalam dokumentasi program.

### Contoh RST reStructuredText

Mari kita ambil contoh teks yang ditulis dalam format file RST sebagai berikut.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Saat teks ini dimasukkan ke prosesor rST seperti Docutils, hasilnya adalah sebagai berikut.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referensi ##

* [reStructuredText - oleh Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

