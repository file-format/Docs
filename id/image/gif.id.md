{
  "date" : "2019-10-11",
  "keywords" :[ "file gif", "format file gif", "apa itu file gif", "file", "contoh gif", "ekstensi file gif", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Format Berkas Gambar",
  "description":"Pelajari tentang format file GIF dan API yang dapat membuat dan membuka file GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GIF? ##

GIF atau Graphical Interchange Format adalah jenis gambar yang sangat terkompresi. Dimiliki oleh Unisys, GIF menggunakan algoritma kompresi LZW yang tidak menurunkan kualitas gambar. Untuk setiap gambar, GIF biasanya mengizinkan hingga 8 bit per piksel dan hingga 256 warna diperbolehkan di seluruh gambar. Berbeda dengan gambar [JPEG](/id/image/jpeg/), yang dapat menampilkan hingga 16 juta warna dan cukup menyentuh batas mata manusia. Kembali ketika internet muncul, GIF tetap menjadi pilihan terbaik karena membutuhkan bandwidth rendah dan kompatibel untuk grafik yang menggunakan area warna yang solid. GIF animasi menggabungkan banyak gambar atau bingkai menjadi satu file dan menampilkannya secara berurutan untuk menghasilkan klip animasi atau video pendek. Batasan warna hingga 256 untuk setiap bingkai dan kemungkinan paling tidak cocok untuk mereproduksi gambar dan foto lain dengan gradien warna.

## Format Berkas GIF ##

Secara konseptual, file GIF memiliki area grafis berukuran tetap yang diisi oleh nol gambar atau lebih. Beberapa file GIF membagi area grafis berukuran tetap atau blok menjadi sub-gambar yang mampu berfungsi sebagai bingkai animasi dalam kasus GIF animasi. Format GIF menggunakan kedalaman piksel 1 hingga 8 bit untuk menyimpan data bitmap. Model warna RGB dan data palet selalu digunakan untuk menyimpan gambar. Bergantung pada versinya, header dengan panjang tetap ("GIF87a" atau "GIF89a") menentukan awal dari file GIF biasa.

Saat ini, tersedia dua versi GIF: 87a dan 89a. Yang pertama adalah format GIF asli sedangkan yang kedua adalah format GIF baru. Dalam format file ini, karakteristik blok dan dimensi piksel disebutkan dalam Deskriptor Layar Logis dengan panjang tetap. Keberadaan dan ukuran Tabel Warna Global dapat ditentukan oleh deskriptor layar, yang melacak detail lebih lanjut jika ada. Cuplikan adalah byte terakhir dari file yang menampung satu byte titik koma ASCII. Tata letak file GIF87a yang khas adalah sebagai berikut:

### Tajuk ###

Header menampung enam byte dan digunakan untuk menentukan jenis file sebagai GIF. Meskipun Deskriptor Layar Logis dipisahkan dari header yang sebenarnya namun terkadang dianggap sebagai header kedua. Struktur yang sama yang digunakan untuk menyimpan header dapat menyimpan Deskriptor Layar Logis. Semua file GIF dimulai dengan tanda tangan 3-byte dan menggunakan karakter "GIF" sebagai pengidentifikasi. Versi ini juga berukuran tiga byte dan menyatakan versi file GIF.

### Deskriptor Layar Logis ###

Deskriptor Gambar dengan panjang tetap menentukan informasi layar dan warna yang diperlukan untuk membuat gambar GIF. Bidang Tinggi dan Lebar menyertakan nilai resolusi layar terkecil, wajib untuk menampilkan data gambar. Jika perangkat tampilan tidak mampu menampilkan resolusi yang ditentukan, penskalaan akan diperlukan untuk menampilkan gambar yang sesuai. Informasi Layar dan Peta Warna ditampilkan oleh empat subbidang tabel di bawah ini (sedangkan bit 0 adalah bit yang paling tidak signifikan):


|Bit|Subbidang
---|---|
|0-2|Ukuran Tabel Warna Global
|3|Warna Meja Sortir Bendera
|4-6|Resolusi Warna
|7|Bendera Tabel Warna Global

#### Tabel Warna Global ####

Tabel Warna Global opsional ditempatkan tepat setelah Deskriptor Layar Logis. Tabel ini dipetakan untuk mengindeks data warna piksel di dalam data gambar. Dengan tidak adanya Tabel Warna Global, setiap gambar dalam file GIF menggunakan Warna Lokalnya. Lebih baik menyediakan tabel warna default jika Tabel Warna Global dan Lokal tidak ada. Serangkaian tripel tiga byte menyusun elemen tabel warna. Setiap byte mencirikan nilai warna RGB. Warna merah, hijau, dan biru digunakan sebagai nilai dari setiap elemen tabel warna. Entri dalam Tabel Warna Global mencapai maksimum 256 entri dan selalu mewakili kekuatan dua.

#### Data Gambar ####

Data gambar menyimpan satu byte simbol yang tidak dikodekan diikuti oleh daftar tertaut dari sub-bersama dengan data yang dikodekan LZW.

#### Cuplikan ####

Cuplikan mewakili satu byte data yang merupakan karakter terakhir dalam file. Nilai byte ini secara permanen 3Bh dan menentukan akhir aliran data. Setiap file GIF harus memiliki cuplikan di akhir setiap file.

## Referensi ##

* [format file GIF](https://en.wikipedia.org/wiki/GIF)

