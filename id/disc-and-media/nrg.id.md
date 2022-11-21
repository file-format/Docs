{
  "date" : "2021-08-16",
  "keywords" :[ "file nrg", "format file nrg", "apa itu file nrg", "file", "contoh nrg", "ekstensi file nrg", "ekstensi", "format", "nrg footer", "file format nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file NRG dan API yang dapat membuat dan membuka file NRG.",
  "title" :"NRG - Format File Gambar Disk",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Apa itu file NRG?

Format file gambar yang dibuat dengan menggunakan cakram optik dianggap sebagai format file NRG. Format ini dibuat khusus oleh Nero untuk keperluan Nero Burning Rom. Untuk penyimpanan gambar disk, format ini dianggap digunakan karena sesuai untuk file khusus ini. File-file ini bisa dalam bentuk salinan persis dari CD atau DVD atau mungkin memiliki beberapa file yang dapat dipasang sebagai disk. Format file lain yang lebih populer seperti format file [ISO](/id/compression/iso/) adalah format file yang dapat dikonversi ke beberapa utilitas dasar. Sebagian besar, file NRG digunakan untuk membuat cadangan atau salinan beberapa data atau disk penting.

## Format File NRG ##

Format file ini dikembangkan oleh Nero AG sebagai format disk image. Itu memiliki properti khusus utilitas Nero Burning Rom karena dikembangkan untuk menyimpan gambar disk. Versi pertamanya ditentukan untuk menyimpan nilai sebagai bilangan bulat 32-bit. Namun, versi keduanya diluncurkan dan berisi dukungan untuk bilangan bulat 64-bit.

## Spesifikasi teknis ##

Di awal file, format ini tidak menyimpan datanya sebagai header. Seperti footer, itu dilampirkan di akhir file. Dalam bentuk potongan IFF, informasi dari gambar disimpan. Offset potongan pertama dapat diperoleh dengan membaca footer NRG pada 8 byte terakhir hingga 12 byte file. Di semua versi format file NRG, ada potongan, DAOI, teks CD, jenis media informasi sesi, informasi disk, Relo, dan akhir rantai yang menyertainya. Urutan byte adalah big-endian dan semua nilai integer tidak ditandatangani pada saat penyimpanan.

### Potongan Utama ###

#### Lembar Isyarat ####

Lembar isyarat ini tersedia dengan mudah di semua versi format file NRG. Potongan **CUEX** berarti blok gabungan ukuran tetap dan masing-masing mewakili titik isyarat.

#### Informasi DAO ####

Informasi ini juga ada di semua versi format NRG. Potongan **DAOI** menyimpan info spesifik yang relevan dalam 2 bagian. Bagian pertamanya hanya terdiri dari data khusus sesi. Bagian keduanya hanya mengulangi informasi abu-abu terkait pelacakan dan hanya sekali untuk setiap trek.

#### CD-teks ####

Ini tersedia dalam versi kedua NRG. Potongan **CDTX** terdiri dari rangkaian mentah paket teks CD yang masing-masing memiliki 18 byte.

#### Informasi Track Diperpanjang ####

Ini tersedia di setiap versi format file NRG. Potongan ini digunakan untuk menyimpan informasi pelacakan untuk trek sesi sekaligus. Data ini diulangi hanya sekali untuk setiap trek.

#### Informasi Sesi ####

Ini juga tersedia di setiap versi format file NRG. Informasi potongan sesi perlu dimanfaatkan untuk memindai gambar sesi dengan cepat dan kemudian melacak hitungan.

#### Akhir rantai ####

Potongan akhir berarti sinyal bahwa sekarang tidak ada potongan lagi yang perlu dibaca dan ini juga tersedia di semua versi NRG.


## Referensi ##

* [NRG - oleh Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


