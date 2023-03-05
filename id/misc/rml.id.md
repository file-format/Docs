{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - File Templat Laporan Elixir",
  "description":"Pelajari tentang file RML dan API yang dapat membuat dan membuka file RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Apa itu file RML?

File RML adalah file template pelaporan dengan mesin pelaporan [Elixir Repertoire](https://elixirtech.com/repertoire-2/). File template digunakan untuk menghasilkan laporan dengan sumber data yang terhubung ke Elixir FileSystem. Data dibaca dan diisi dalam file template RML dan dapat diekspor ke beberapa format file yang berbeda seperti [PDF](/id/pdf/), [RTF](/id/word-processing/rtf/), dan spreadsheet [XLS](/id/spreadsheet/xls/). Mesin pelaporan Repertoar Elixir dapat dihubungkan ke berbagai sumber data JDBC.

## Format File RML

Detail struktur file internal format file RML tidak tersedia untuk umum. File dibuat dan disimpan secara internal oleh aplikasi Elixir Repertoire untuk menghasilkan laporan dengan data yang diisi dari sumber data yang terhubung. File template RML berisi tata letak keseluruhan dan informasi placeholder dari laporan akhir yang dihasilkan dari data.

## Bagaimana cara File Templat RML?

Untuk menghasilkan template RML di Elixir Repertoar, langkah-langkah berikut dapat diikuti.

1. Sambungkan sumber data JDBC ke sistem file.
1. Luncurkan Panduan Templat Laporan
1. Gunakan perangkat lunak untuk menemukan file .ds sumber data
1. Pilih laporan tabular sebagai pilihan ekspor
1. Pilih bidang yang akan disertakan dalam template laporan
1. Terakhir, saat mengklik tombol Finish, First report.rml ditambahkan ke repositori dan dibuka untuk menampilkan tab Layout.

## Referensi

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)

