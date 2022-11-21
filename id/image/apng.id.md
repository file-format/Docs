{
  "date" : "2019-10-11",
  "keywords" :[ "file apng", "format file apng", "apa itu file apng", "file", "contoh apng", "ekstensi file apng", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File APNG - File Grafis Jaringan Portabel Animasi",
  "description":"Pelajari tentang format file APNG dan API yang dapat membuat dan membuka file APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file APNG?

File dengan ekstensi .apng (Animated Portable Network Graphics) adalah format grafik raster dan merupakan ekstensi tidak resmi untuk Grafik Jaringan Portabel ([PNG](/id/image/png/) ). Ini terdiri dari beberapa frame (masing-masing gambar PNG) yang mewakili urutan animasi. Ini memberikan visualisasi yang mirip dengan file [GIF](/id/image/gif/). File APNG mendukung gambar 24-bit dan transparansi 8-bit. APNG kompatibel dengan file GIF non-animasi. File APNG menggunakan ekstensi .png yang sama dan dapat dibuka oleh aplikasi seperti Mozilla Firefox, Chrome dengan dukungan APNG, aplikasi iMessage untuk iOS 10.

## Sejarah Singkat

* Spesifikasi APNG dibuat pada tahun 2004 untuk mendukung Gambar PNG animasi
* Decoder APNG dikembangkan dengan ukuran yang jauh lebih kecil dan menggunakan dekoder PNG bagian belakang
* Setelah pertimbangan terus-menerus, image/apng tipe MIME baru diformulasikan sambil menjaga ekstensi tetap sama dengan .png, bukan .apng
* APNG secara resmi ditolak oleh grup PNG pada tanggal 20 April 2007 karena keseragaman gambar PNG sekaligus memiliki spesifikasi yang berbeda

## Format File APNG

File APNG disimpan sebagai file biner pada disk dan menggunakan spesifikasi PNG yang diperluas untuk gambar animasi. Bingkai pertama file APNG adalah aliran PNG normal yang dapat dibaca oleh dekoder PNG untuk ditampilkan. Format file APNG mengikuti spesifikasi PNG dan data disimpan dalam segmen-segmen yang disebut chunks. Namun, APNG memperkenalkan potongan baru berikut:

`Potongan Kontrol Animasi (acTL)` - Menunjukkan bahwa file ini adalah file PNG animasi, bukan file PNG normal. Ini bertindak sebagai penanda dan muncul sebelum potongan IDAT. Ini juga berisi jumlah bingkai dan informasi tentang waktu untuk mengulang animasi

`Bingkai Kontrol Bingkai` - Terjadi di awal setiap dan informasi metadata seperti dimensi, posisi, aplikasi transparansi, dan informasi penggantian oleh bingkai sebelumnya atau berikutnya setelah selesai.

`Frame Data Chunk` - Menyimpan konten bingkai dan dimulai dengan nomor urut. Nomor urut ini memiliki struktur yang sama dengan potongan IDAT gambar default.

{{< figure src="../APNG.png" alt="PNG Animasi - Format File APNG" >}}

APNG kompatibel dengan PNG karena spesifikasi lateral dirancang sedemikian rupa sehingga aplikasi yang membaca file PNG seharusnya mengabaikan potongan yang tidak dimengerti. Spesifikasi mengenai kedalaman bit, jenis warna, kompresi, filter, metode interlace, dan informasi palet digunakan sama dengan format PNG default.

## APNG vs GIF

Dengan GIF yang sudah ada dan digunakan dalam jangka waktu yang lama, Anda mungkin bertanya-tanya apa bedanya APNG dengan GIF. Berikut adalah perbandingan antara APNG dan GIF yang memberikan gambaran singkat tentang kedua format file tersebut.

||APNG|GIF|
---|---|---|
|Diterbitkan|2004|1987|
|Kedalaman Warna|24 bit|8 bit|
|Frame Rate|Unlimited|10 frame per detik|
|Transparansi|Lengkap dan sebagian|Lengkap|
|Kompresi|Sangat Bagus|Bagus|

## Referensi

* [Format File APNG](https://en.wikipedia.org/wiki/APNG)
* [Spesifikasi Format PNG Resmi](https://www.w3.org/TR/PNG/)

