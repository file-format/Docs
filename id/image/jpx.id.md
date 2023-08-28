{
  "date" : "2021-02-10",
  "keywords" :[ "file jpx", "format file jpx", "apa itu file jpx", "file", "contoh jpx", "ekstensi file jpx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Format Berkas Gambar",
  "description":"Pelajari tentang format file JPX dan API yang dapat membuat dan membuka file JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Apa itu file JPX? ##

File dengan ekstensi .jpx adalah ekstensi untuk format file JPEG 2000. Ini menggunakan kompresi JPEG 2000 terutama dan juga menyediakan fitur-fitur canggih seperti banyak lapisan untuk gambar, berbagai ruang warna, opasitas, dan aliran kode yang terfragmentasi. JPX juga memungkinkan kompresi lain seperti JBIG, CCITT Group3, CCITT Group4, dll. Selain kompresi JPEG 2000. Format file JPX telah disetujui sebagai standar [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), tetapi tidak dapat menerima sambutan hangat karena penggunaan ekstensif [JPEG ](/id/image/jpeg/) format file. Aplikasi yang bisa membuka file JPX antara lain Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020, dan CorelDraw Graphics Suite 2020.

## Sejarah Singkat

Pada tahun 2000, komite Joint Photographic Experts Group merancang JP2 dengan tujuan untuk meningkatkan standar JPEG berbasis transformasi kosinus diskrit mereka sendiri dengan metode berbasis gelombang kecil ini. Komite JPEG bertujuan untuk menyediakan metode dasar mereka tanpa biaya lisensi. Dalam lisensi JP2 yang mendapatkan persaingan di antara 20 perusahaan, mereka menang tipis. JPEG 2000 telah dinyatakan sebagai standar ISO, meskipun sebagian besar browser web belum siap untuk membantu JPEG 2000 sejak 2017. Pada tahun 2004, format ISO/IEC 15444-2 diterima secara publik sebagai ekstensi ke format file JP2.

## Format File JPX

Format file JPX diformulasikan untuk memenuhi persyaratan aplikasi yang membutuhkan struktur data di luar fungsionalitas yang ditentukan oleh format file [JP2](/id/image/jp2/). File JP2 dengan ekstensi yang tidak kompatibel dapat menyebabkan kebingungan di pasar di mana beberapa pembaca dapat menginterpretasikan beberapa file JP2 tetapi tidak yang lain. JPX adalah jawaban untuk menghindari masalah seperti itu di aplikasi.

### Identifikasi Berkas

File JPX disimpan sebagai [JPF](/id/image/jpf/) saat disimpan dalam sistem file komputer tradisional. Itu sebabnya istilah JPX paling tidak umum digunakan dibandingkan dengan JPF. File JPX dimulai dengan byte berikut:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organisasi Berkas

Mirip dengan JP2, file JPX adalah kumpulan kotak yang memiliki struktur biner dengan kotak yang disusun dalam urutan yang berdekatan. Kotak pertama memberikan awal ke file dengan byte pertama dan byte terakhir dari kotak terakhir mewakili byte terakhir dari file.
Struktur biner kotak dalam file JPX identik dengan yang ditentukan dalam format file [JP2](/id/image/jp2/).

### Penyimpanan CodeStream di JPX

Format file JPX memungkinkan codestream gambar dibagi menjadi beberapa fragmen. Ini memungkinkan untuk memodifikasi satu ubin gambar dan menulis ubin yang dimodifikasi ke akhir file tanpa menulis ulang seluruh file. Format file [JP2](/id/image/jp2/) asli membatasi seluruh codestream untuk disimpan dalam porsi file yang berdekatan, yang dapat menjadi masalah bagi aplikasi pengeditan gambar yang mungkin ingin mengubah satu petak gambar dan mencapai dukungan di atas dengan format file JPX. Fragmentasi codestream gambar membuat format file JPX lebih unggul daripada format file JP2. Selain itu, format file JPX memungkinkan beberapa aliran kode digabungkan dan menghasilkan hasil yang dirender. Codestreams dapat digabungkan sebagai pengomposisian dan animasi.

## Referensi ##

* [Ringkasan JPEG 2000](https://jpeg.org/jpeg2000/)

