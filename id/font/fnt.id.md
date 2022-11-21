{
  "date" : "2020-08-20",
  "keywords" :[ "file fnt", "format file fnt", "apa itu file fnt", "file", "contoh fnt", "ekstensi file fnt", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - File Font Windows",
  "description":"Pelajari tentang format file FNT dan API yang dapat membuat dan membuka file FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Apa itu berkas FNT?

File dengan ekstensi .fnt adalah file font yang menyimpan informasi font umum pada sistem Operasi Windows. File FNT sebagian besar telah digantikan oleh format file TrueType (.TTF) dan OpenType (.OTF), dan merupakan format file font yang sudah usang seperti sekarang. File-file ini dapat menyimpan satu font rater atau vektor. Semua driver perangkat mendukung font Windows 2.x. Namun, tidak semua driver perangkat
mendukung versi Windows 3.0.

## Format File FNT

File FNT mampu menyimpan satu font raster atau vektor. Format vektor lebih sering digunakan oleh GDI dibandingkan dengan raster di mana mesin terbang masing-masing charter didefinisikan menggunakan bitmap kecil. Alasan yang jelas untuk mengganti .fnt dengan .ttf dan .otf adalah format rasternya.

### Kepala File Font
Awal file font raster dan vektor adalah umum, diikuti dengan informasi yang berbeda untuk setiap jenis file. Header file font termasuk untuk Windows 3.0 mencakup enam bidang baru sebagai berikut yang diatur ke nol untuk memastikan kompatibilitas dengan versi windows yang akan datang.

* dFlag
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

Untuk informasi mendetail tentang header untuk Windows 3.0 dan 2.0, kunjungi [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referensi
* [Format File Font](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Cara menginstal atau menghapus font di Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

