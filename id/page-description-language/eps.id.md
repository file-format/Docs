{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "file", "ekstensi", "format file", "Tata Letak Halaman", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file EPS dan API yang dapat membuat dan membuka file EPS.",
  "title" :"Format File EPS - File PostScript Terenkapsulasi",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file EPS?

File .eps adalah file gambar yang disimpan ke disk dalam format file Encapsulated Postscript. Ini mungkin berisi kombinasi teks, grafik, dan gambar. File EPS juga dapat menyertakan gambar pratinjau bitmap yang dikemas di dalamnya untuk ditampilkan oleh aplikasi yang dapat membuka file tersebut.

## Sejarah Singkat Format File EPS

Sekilas tentang format file EPS dari perspektif sejarah mengungkapkan informasi berikut:

* Versi pertama EPS dirilis oleh Adobe antara tahun 1985 dan 1988
* Versi 2.0 dari spesifikasi EPS diterbitkan pada Januari 1989
* Spesifikasi EPS versi 3.0 diterbitkan sebagai dokumen terpisah pada tahun 1992; ini adalah versi terbaru yang diterbitkan.

EPS, dalam kombinasi dengan mekanisme ekstensi Open Structuring Conventions yang dijelaskan dalam pasal 9 dari Spesifikasi Konvensi Penataan Dokumen Bahasa PostScript Adobe, membentuk dasar dari versi awal format file Karya Seni Adobe Illustrator.

## Berformat EPS

EPS adalah format berpemilik tetapi didokumentasikan secara publik dan spesifikasi format file EPS tersedia untuk umum sebagai referensi pengembang. EPS adalah [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Konvensi Penataan Dokumen) yang menyesuaikan format file dan mematuhi semua aturan yang ditetapkan oleh DSC. DSC adalah format file khusus untuk dokumen PostScript oleh Adobe. Aplikasi apa pun yang mengklaim dapat membaca file EPS harus sesuai dengan DSC.

File EPS terdiri dari dua bagian utama seperti yang dijelaskan di bawah ini.

### Pratinjau Gambar ###

File EPS tipikal berisi gambar pratinjau dalam format yang ditujukan untuk kenyamanan penggunaan dalam alur kerja yang melibatkan beberapa sistem atau aplikasi. Maksud pratinjau adalah memiliki gambar dalam format yang dapat dirender oleh sebagian besar aplikasi grafis; pratinjau biasanya memiliki resolusi lebih rendah, dalam dimensi piksel dan/atau kedalaman bit. File pratinjau bisa dalam salah satu dari sejumlah format. Spesifikasi untuk EPS_3 mencantumkan tiga format pratinjau "khusus perangkat":

* untuk Apple Macintosh, gambar PICT seperti yang digunakan oleh aplikasi QuickDraw
* untuk komputer DOS, bitmap TIFF
* File Meta Windows.

PICT dan Windows Metafile dapat menggabungkan data bitmap dan grafik vektor. Selain itu, spesifikasi menentukan representasi independen perangkat yang sangat sederhana untuk gambar pratinjau bitmap yang disematkan. Representasi ini dikenal sebagai Encapsulated PostScript Interchange Format (EPSI).

Pratinjau EPSI adalah bitmap yang direpresentasikan sebagai heksadesimal ASCII, terbungkus di antara beberapa komentar PostScript untuk identifikasi dan dimaksudkan agar sederhana dan mudah dipindahkan. Untuk membedakan file EPS dengan format pratinjau yang berbeda, ekstensi file DOS dan jenis file Macintosh yang berbeda direkomendasikan dalam spesifikasi EPS.

### Kode PostScript

Minimal, format file EPS harus menyertakan yang berikut ini:

* komentar tajuk, %!PS-Adobe-3.0 EPSF-3.0
* dan komentar kotak pembatas, %%BoundingBox: llx lly urx ury, yang menjelaskan batasan ilustrasi. Keempat argumen ini sesuai dengan sudut kiri bawah (llx, lly) dan kanan atas (urx, ury) dari kotak pembatas.

File EPS tidak dapat menggunakan operator berikut:

* perangkat band,
* cleardictstack
* halaman salinan
* hapus halaman
* server keluar
* bingkai perangkat
*grestoreall
* initclip
* initgraphics
* initmatrix
* berhenti
* renderband
* setglobal
* setpagedevice
* setshared
* mulai pekerjaan.

## Konversi EPS ke format File Lain

File EPS dapat dikonversi ke format gambar standar seperti [JPG](/id/image/jpeg/), [PNG](/id/image/png/), [TIFF](/id/image/tiff/), dan [PDF](/id/pdf/) menggunakan aplikasi yang berbeda misalnya Adobe Illustrator, Photoshop dan PaintShop Pro.

Karena [kerentanan keamanan](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) dalam file EPS, Office 2016, Office 2013, Office 2010, dan Office 365 telah menonaktifkan kemampuan untuk memasukkan file EPS ke dalam dokumen Office.

## Referensi

* [Encapsulated PostScript - Oleh Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

