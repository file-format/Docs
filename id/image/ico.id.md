{
  "date" : "2019-10-11",
  "keywords" :[ "file ico", "format file ico", "apa itu file ico", "file", "contoh ico", "ekstensi file ico", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Format File Gambar",
  "description":"Pelajari tentang format file ICO dan API yang dapat membuat dan membuka file ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ICO?

File dengan ekstensi ICO adalah jenis file gambar yang digunakan sebagai ikon untuk representasi aplikasi di [Microsoft Windows](https://www.microsoft.com/en-us/windows). Ini datang dalam berbagai ukuran, dukungan warna dan resolusi yang sesuai dengan persyaratan tampilan. Format file gambar serupa lainnya di Microsoft Windows adalah [CUR](/id/image/cur/) untuk representasi kursor dan menentukan hotspot di header gambar. Di MacOS, format file ICNS memiliki tujuan yang sama dengan file ICO. Beberapa situs web online serta aplikasi menyediakan fitur untuk membuat file tersebut dan mengonversi format gambar lain seperti [BMP](/id/image/bmp/), [PNG](/id/image/png/), dll. ke format file ikon. Jenis media Internet terdaftar IANA resmi untuk file ICO adalah image/vnd.microsoft.icon.

## Sejarah Singkat ##

Ikon diperkenalkan dengan peluncuran Microsoft Windows 1.0. Ini berukuran 32x32 dan monokrom. Dengan kedatangan win32, dukungan untuk gambar ikon dalam warna asli diperkenalkan dengan dimensi hingga 256x256 piksel. Windows XP adalah yang pertama memberikan dukungan untuk gambar ikon warna 32-bit, memungkinkan area semi-transparan seperti bayangan, anti-aliasing, dan efek seperti kaca ditambahkan ke ikon. Microsoft hanya merekomendasikan ukuran ikon hingga 48×48 piksel untuk Windows XP. Windows Vista menambahkan tampilan ikon 256×256 piksel ke Windows Explorer, serta dukungan untuk format [PNG](/id/image/png/) terkompresi. Dengan pengguna yang menggunakan resolusi lebih tinggi dan mode DPI tinggi, format ikon yang lebih besar (seperti 256×256) direkomendasikan.

## Format File ICO ##

Satu file ICO terdiri dari satu atau lebih dari satu gambar kecil dengan berbagai ukuran dan kedalaman warna. Kehadiran gambar dengan berbagai ukuran adalah untuk penskalaan yang sesuai pada resolusi layar yang berbeda. Semua nilai dalam file ICO/CUR direpresentasikan dalam urutan byte [little-endian](https://en.wikipedia.org/wiki/Little-endian).

File ICO terdiri dari header Ikon, Direktori Ikon,

|Bidang|Deskripsi
---|---|
|Icon Header|Menyimpan informasi umum tentang file ICO.
|Direktori[1..n]|Menyimpan informasi umum tentang setiap gambar dalam file.
|Ikon #1|"Data" sebenarnya untuk gambar pertama dalam format AND/XOR DIB lama atau PNG yang lebih baru
|...|
|Icon #n|Data untuk gambar ikon terakhir

### Tajuk ###

|Offset|Ukuran (dalam byte)|Tujuan
---|---|---|
|0|2|Dicadangkan. Harus selalu 0.
|2|2|Menentukan jenis gambar: 1 untuk gambar ikon (.ICO), 2 untuk gambar kursor (.CUR). Nilai lainnya tidak valid.
|4|2|Menentukan jumlah gambar dalam file.

### Direktori ###

Direktori yang terdapat dalam file ICO, direpresentasikan sebagai struktur ICONDIR, berisi struktur ICONDIRECTORY untuk setiap gambar dalam file. Hal yang sama diikuti oleh blok yang berdekatan dari semua data bitmap gambar. Ini seperti yang ditunjukkan di bawah ini.

|Offset|Ukuran|Deskripsi
---|---|---|
|0 (0)|1|Lebar, harus 0 jika 256 piksel
|1 (1)|1|Tinggi, harus 0 jika 256 piksel
|2 (2)|1|Jumlah warna, harus 0 jika lebih dari 256 warna
|3 (3)|1|Dicadangkan, harus 0
|4 (4)|2|Pesawat warna saat dalam format .ICO, harus 0 atau 1, atau hotspot X saat dalam format .CUR
|6 (6)|2|Bits per piksel saat dalam format .ICO, atau hotspot Y saat dalam format .CUR
|8 (8)|4|Ukuran data bitmap dalam byte.
|12 (C)|4|Offset dalam file.

## Referensi ##

* [ICO - Oleh Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

