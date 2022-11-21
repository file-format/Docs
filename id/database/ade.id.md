{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file ADE dan API yang dapat membuat dan membuka file ADE.",
  "title" :"ADE - Akses File Ekstensi Proyek",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Apa itu file ADE?

File dengan ekstensi .ade adalah file Microsoft Access Project yang berisi hasil kompilasi dari informasi yang terkandung dalam file proyek Microsoft Access ADP. Informasi dalam file proyek Access, selain Visual Basic for Applications (VBA), tersedia dalam bentuk terkompilasi dalam file ADE. Data disimpan dalam format terkompresi dalam file ini untuk mengurangi ukuran file dan meningkatkan kinerja di Access. Karena ADE adalah keluaran terkompilasi dari file proyek Access, setiap kode sumber VBA yang merupakan bagian dari proyek, tetap dilindungi dengan tidak mengizinkannya menjadi bagian dari keluaran. File ADE dapat dibuka di Microsoft Access 365.

## Format File ADE - Informasi Lebih Lanjut

ADE adalah file Access Database yang dikompilasi yang disimpan ke disk sebagai file biner. Struktur file internal dari file-file ini tidak diketahui.

File ADE dapat menimbulkan masalah saat dibuka berdasarkan versi Microsoft Access yang telah digunakan untuk membuat file tersebut. Access database yang menggunakan Microsoft Access 2010 versi 64-bit dan yang dikompilasi sebagai file MDE, [ACCDE](/id/database/accde/), atau ADE harus dikompilasi ulang di Microsoft Access 2021 Paket Layanan 1 (SP1) untuk bekerja dengan benar dengan Access 2010 SP1. Masalah ini terjadi karena Access 2010 SP1 menggunakan versi terbaru dari berkas VBE7.dll (versi 7.00.1619).

## Referensi

* [Masalah dengan Access ADE Files](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Format File Akses Mana yang Digunakan](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

