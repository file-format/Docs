{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "file", "ekstensi", "format file", "Mathematica", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang apa itu API file NB yang dapat membuat dan membuka file NB.",
  "title" :"NB - Format Berkas Notebook Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Apa itu file NB?

File dengan ekstensi .nb adalah format file notebook Wolfram yang menyimpan instruksi instruksi matematika dalam file tekstual. Itu dapat berisi berbagai jenis data seperti perhitungan langsung, antarmuka dinamis arbitrer, input typeset lengkap, input gambar, anotasi kode otomatis, antarmuka program tingkat tinggi yang lengkap, dan ribuan fungsi dan opsi yang diatur dengan hati-hati. Instruksi tekstual adalah input dan output Mathematica yang dihasilkan dan diperbarui saat pernyataan input dimasukkan ke dalam file.

## Format File Wolfram Notebook NB - Informasi Lebih Lanjut

File Wolfram Notebook NB disimpan dalam format teks biasa yang merupakan format file yang dapat dibaca manusia. Konten buku catatan diatur dalam bagian sebagai teks biasa yang masing-masing diwakili oleh grup sel, mirip dengan Spreadsheet. Kisaran kelompok-kelompok ini ditentukan oleh tanda kurung menjelang akhir setiap sel. Gaya yang ditetapkan ke sel menentukan perannya dalam buku catatan seperti yang dijelaskan di bawah ini.

### Buku Catatan sebagai Bahasa Wolfram

Ketika dimaksudkan untuk menyimpan Notebook yang terdiri dari instruksi matematika untuk dieksekusi oleh Wolfram Language Kernal, sel-sel dalam dokumen secara otomatis diberi gaya teks `Input`. Ini memberi tahu kernal untuk menganggap ini sebagai instruksi yang dijalankan saat pengguna mengeluarkan kombinasi tombol `Shift+Return`. Notebook Mathematica seperti yang ditunjukkan pada contoh berikut.

{{< figure src="../Wolfram Notebook.jpeg" alt="Format File Buku Catatan Wolfram" >}}

### Notebook sebagai Dokumen

Notebook Mathematica dapat dalam format dokumen untuk memberikan gambaran tentang apa yang Anda lihat apa yang Anda dapatkan (WYSIWYG). Dokumen-dokumen ini sama seperti yang dilihat di layar atau di kertas cetak, dan bersifat interaktif. Untuk ini, `Text Style` ditetapkan ke sel untuk menampilkan konten tanpa mengeksekusi pernyataan oleh Kernel.

## Ekspor Buku Catatan Mathematica

Notebook Mathematica dapat diekspor ke berbagai format file seperti PDF, grafik, GIS, Compressed, dan Spreadsheets.

## Referensi

* [Dasar-Dasar Buku Catatan Mathematica](https://reference.wolfram.com/language/guide/NotebookBasics.html)

