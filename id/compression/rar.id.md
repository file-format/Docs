{
  "date" : "2019-10-11",
  "keywords" :[ "file rar", "format file rar", "apa itu file rar", "file", "contoh rar", "ekstensi file rar", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Apa itu ekstensi file RAR dan API yang dapat membuat dan membuka file RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file RAR?

File dengan ekstensi .rar adalah file arsip yang dibuat untuk menyimpan informasi dalam bentuk terkompresi atau normal. RAR, yang merupakan singkatan dari format file Roshal ARchive, adalah format file berpemilik yang dibuat oleh Eugene Roshal pada tahun 1995 yang merupakan seorang insinyur perangkat lunak Rusia. Format ini digunakan untuk mengarsipkan file dengan berbagai metode termasuk berbagai teknik kompresi. Ada beberapa perangkat lunak aplikasi yang tersedia untuk Windows, Linux dan MacOS untuk mengekstrak file RAR. Perangkat lunak WinRAR, oleh RARLab, adalah utilitas pengarsipan file shareware (gratis selama 40 hari) untuk platform Microsoft Windows; perangkat lunak tersebut dipindahkan ke Linux (hanya sebagai ekstraktor) oleh Penulis yang sama, Eugene Roshal.

## Sejarah Versi Format File RAR

* v1.3 (asli, tidak memiliki tanda tangan "Rar!")
* v1.5
* v2.0 - dirilis dengan WinRAR 2.0 dan Rar untuk MS-DOS 2.0
* v2.9 - dirilis di WinRAR versi 3.00
* v5.0 - didukung oleh WinRAR 5.0 dan yang lebih baru

## Fitur Utama Format RAR

RAR telah berada di lapangan cukup lama dan telah menjadi salah satu format file pengarsipan favorit. Fitur utama tentang format RAR adalah:

**`Rasio kompresi tinggi:`** Unggul dibandingkan dengan [ZIP](/id/compression/zip/), sebanding dengan format 7z dan zipx.

**`Enkripsi file yang kuat dengan desain:`** Arsip RAR4 terenkripsi mengandalkan enkripsi berbasis AES-128 sementara arsip RAR5 terenkripsi mengandalkan enkripsi AES-256 dengan penjadwalan kunci yang ditingkatkan

**`Kemampuan koreksi kesalahan lanjutan dan pemulihan data:`** rekaman pemulihan opsional selama pembuatan arsip

**`Ukuran File:`** Berukuran minimal 20 byte dan maksimal 2^63 byte (8 exabyte dari total ukuran arsip)

**`Arsip RAR multi-volume:`** Kemungkinan untuk membagi arsip besar menjadi beberapa file yang lebih kecil untuk memfasilitasi transfer melalui jaringan. Dalam kasus seperti itu, ekstensi file bertambah 1 untuk mewakili volume terpisah

## Berformat RAR

Spesifikasi lengkap format RAR tidak tersedia untuk umum dan karena itu detail tentang format tidak dapat dirumuskan secara ringkas.

### Tata Letak Arsip Umum

Tata letak umum format file RAR yang diperkenalkan di versi 5.0 adalah sebagai berikut:

|Format Berkas
---|
|Modul self-extracting (opsional)
|RAR 5.0 Tanda Tangan
| Header Enkripsi Arsip (opsional)
| Tajuk Arsip Utama
|Arsipkan tajuk layanan komentar (opsional)
Judul File 1
| Header Layanan (NTFS ACL, stream, dll.) untuk file sebelumnya (opsional)
|...
|Berkas Tajuk N
| Header Layanan (NTFS ACL, stream, dll.) untuk file sebelumnya (opsional)
|Rekaman Pemulihan (opsional)
|Akhir dari tajuk arsip

Informasi tentang setiap bagian file RAR yang disebutkan di atas dapat ditemukan di dokumen [Spesifikasi Format File RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Mengekstrak Sendiri Arsip RAR

Jika file RAR itu sendiri diekstraksi sendiri, informasi yang diekstraksi sendiri terdapat di awal file sebelum tanda tangan arsip. Ukuran dan isinya tidak ditentukan.

#### Tanda Tangan RAR 5.0

Tanda tangan RAR adalah header 8-byte yang terdiri dari angka ajaib berikut:

0x52 61 72 21 1A 07 00

di mana

0x6152 - KEPALA_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referensi

* [Format Arsip RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - Oleh Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

