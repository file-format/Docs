{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "file ma", "format file ma", "format file", "3d", "unduhan file ma", "file .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file MA dan API yang dapat membuka dan membuat file MA.",
  "title" :"Format File MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Apa itu file MA?

File dengan ekstensi .ma adalah file proyek 3D yang dibuat dengan aplikasi Autodesk Maya. Ini berisi daftar besar perintah tekstual untuk menentukan informasi tentang file. File **.ma** dapat dibuka dan diedit di editor teks apa pun untuk memperbaiki masalah apa pun dengan perintah jika file rusak. File-file ini berisi informasi untuk menentukan informasi Pemandangan 3D seperti geometri, pencahayaan, animasi, dan rendering.

## Format File MA

File MA disimpan ke disk dalam format teks ASCII tidak seperti file MB yang disimpan dalam format file biner ke disk. Referensi mendetail untuk format file MA tersedia di [Dokumentasi Autodesk Maya](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) dan dapat dirujuk untuk referensi pengembang.

### Kepala Berkas MA

Header file MA dimulai dengan bagian komentar yang memberikan informasi pembuatan file dan tanggal modifikasi. Pembaca file Maya mengabaikan blok ini karena hanya digunakan untuk tujuan informasi saja. Header harus dimulai dengan enam karakter pertama sebagai "//Maya".

Header file ASCII terlihat seperti berikut.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Referensi Berkas

Bagian referensi file dari file .ma berisi informasi tentang semua file Maya lain yang dirujuk dalam file ini. Setiap file yang direferensikan dapat dibaca menggunakan satu perintah file yang terkandung dalam file yang sama. Sintaks perintah file saat digunakan untuk referensi adalah:

```
file -r -rpr prefixString fileName;
```
atau

```
file -r -ns nameSpace fileName
```
Berikut adalah contoh string.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Contoh ini menunjukkan bahwa objek matahari yang ada di file `solar` akan dapat diakses di file ini menggunakan nama "solar_sun".

### Persyaratan

Bagian persyaratan dari file .ma terdiri dari serangkaian perintah yang diperlukan dan memberi tahu informasi Mei seperti informasi versi dan plugin yang diperlukan untuk membaca file. Contoh bagian persyaratan adalah sebagai berikut.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Bagian selanjutnya menentukan persyaratan. Ini terdiri dari serangkaian perintah yang membutuhkan. Bagian file ini memberi tahu Maya perangkat lunak apa yang diperlukan untuk memuat file dengan benar. Secara khusus, versi Maya apa, dan plug-in apa.

## unduhan file MA
Agak sulit untuk menemukan dan mengunduh file MA dari model 3d. Oleh karena itu, Anda dapat mengunduh file MA sampel dari sini:

- [Sampel.ma](../sample.ma)


## Referensi

* [Organisasi File ASCII Maya - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

