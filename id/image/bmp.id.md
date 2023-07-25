{
  "date" : "2019-10-11",
  "keywords" :[ "file bmp", "format file bmp", "apa itu file bmp", "file", "contoh bmp", "ekstensi file bmp", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Format Berkas Gambar",
  "description":"Pelajari tentang format file BMP dan API yang dapat membuat dan membuka file BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Apa itu file BMP? #

File berekstensi .BMP merupakan file Gambar Bitmap yang digunakan untuk menyimpan gambar digital bitmap. Gambar-gambar ini tidak tergantung pada adaptor grafis dan juga disebut format file device independent bitmap (DIB). Kemandirian ini berfungsi untuk membuka file di berbagai platform seperti Microsoft Windows dan Mac. Format file BMP dapat menyimpan data sebagai gambar digital dua dimensi baik dalam format monokrom maupun warna dengan berbagai kedalaman warna.

## Spesifikasi Format File BMP ##

Device Independent Bitmaps bertindak sebagai bantuan untuk bertukar bitmap antara perangkat dan aplikasi. Karena evolusi berkelanjutan dari format file ini, informasi yang terkandung dalam header dapat berbeda sesuai versi Bitmap. File bitmap tunggal terdiri dari struktur ukuran tetap dan variabel dalam urutan tertentu.

Struktur dalam file Bitmap disusun dengan urutan sebagai berikut:


|Struktur|Opsional|Ukuran|Tujuan
---|---|---|---|
|File Header|No|14|Untuk menyimpan informasi umum tentang file gambar bitmap
|DIB Header|No|Fixed-Size|Untuk menyimpan informasi detail tentang gambar bitmap dan menentukan format piksel
|Masker Bit Ekstra|Ya|12 atau 16 byte|Untuk menentukan format piksel
|Palet Warna|Semi-opsional|Ukuran variabel|Untuk menentukan warna yang digunakan oleh data gambar bitmap
|Gap1|Ya|Ukuran variabel|Perataan struktur
|Pixel Array|No|Variable-size|Format piksel ditentukan oleh header DIB atau masker bit ekstra.
|Gap2|Ya|Ukuran variabel|Perataan struktur
|Profil Warna ICC|Ya|Ukuran variabel|Untuk menentukan profil warna untuk manajemen warna

Ketika gambar bitmap dimuat ke dalam memori, itu menjadi struktur DIB, yang digunakan oleh Windows melalui API GDI-nya. Header File bukan bagian dari struktur data ini. Warna juga dapat terdiri dari entri 16-bit yang merupakan indeks ke palet yang direferensikan saat ini, bukan definisi warna RGB eksplisit. Mari kita lihat beberapa di antaranya secara mendetail, terutama header.

### Kepala Berkas Bitmap ###

Header File Bitmap mirip dengan header file lain yang digunakan untuk mengidentifikasi file. Karena ada varian yang berbeda untuk format file BMP, 2 byte pertama dari format file BMP adalah karakter "B" dan kemudian karakter "M" dalam pengkodean ASCII. Semua nilai integer disimpan dalam format little-endian.

|Offset hex|Offset dec|Ukuran|Tujuan
---|---|---|---|
|00|0|2 byte|Kolom header yang digunakan untuk mengidentifikasi file BMP dan DIB adalah 0x42 0x4D dalam heksadesimal, sama seperti BM dalam ASCII. Itu dapat mengikuti nilai yang mungkin.* **BM** – Windows 3.1x, 95, NT, ... dll. * **BA** – OS/2 struct bitmap array * **CI** – OS/2 struct ikon warna * **CP** – penunjuk warna const OS/2 * **IC** – ikon struktur OS/2 * **PT** – penunjuk OS/2
|02|2|4 byte|Ukuran file BMP dalam byte
|06|6|2 byte|Dicadangkan; nilai sebenarnya tergantung pada aplikasi yang membuat gambar
|08|8|2 byte|Dicadangkan; nilai sebenarnya tergantung pada aplikasi yang membuat gambar
|0A|10|4 byte|Offset, yaitu alamat awal, dari byte tempat data gambar bitmap (larik piksel) dapat ditemukan.

#### DIB header (header informasi bitmap) ####

Informasi mendetail tentang gambar diwakili oleh tajuk ini. Berdasarkan informasi tersebut, akan ditentukan aplikasi yang akan digunakan untuk menampilkan gambar pada layar. Semua tajuk tersebut berisi bidang DWORD (32-bit), yang menentukan ukurannya, sehingga aplikasi dapat dengan mudah menentukan tajuk yang digunakan dalam gambar. Ini pada dasarnya disebabkan oleh fakta bahwa format DIB mengalami beberapa ekstensi. Berikut adalah Header DIB dengan bidang yang terdaftar.

#### Palet warna ####

Palet warna BMP adalah larik struktur yang menentukan nilai intensitas RGB setiap warna dalam palet warna perangkat layar. Setiap piksel dalam data bitmap menyimpan satu nilai yang digunakan sebagai indeks ke dalam palet warna. Informasi warna yang disimpan dalam elemen pada indeks tersebut menentukan warna piksel tersebut. Ketersediaan warna pada file bitmap bervariasi sebagai berikut:

* Satu, 4 dan 8-bit - diharapkan selalu berisi palet warna
* Enam belas, 24 dan 32-bit - tidak pernah mengandung palet warna
* File BMP enam belas dan 32-bit - berisi nilai topeng bitfield sebagai pengganti palet warna

#### Penyimpanan Piksel ####

Piksel bitmap disimpan sebagai bit yang dikemas dalam baris di mana ukuran setiap baris dibulatkan menjadi kelipatan 4 byte (DWORD 32-bit) dengan padding. Jumlah total byte yang diperlukan untuk menyimpan piksel suatu gambar tidak dapat langsung dihitung dengan hanya menghitung bit. Karena ada bantalan yang terlibat, efek membulatkan ukuran setiap baris menjadi kelipatan 4 byte diperlukan. Padding byte (tidak harus 0) harus ditambahkan ke akhir baris untuk menaikkan panjang baris menjadi kelipatan empat byte. Saat array piksel dimuat ke dalam memori, setiap baris harus dimulai pada alamat memori yang merupakan kelipatan 4.

Gambar sebenarnya dijelaskan oleh representasi DWORD 32-bit dari susunan piksel. Biasanya piksel disimpan "dari bawah ke atas", mulai dari pojok kiri bawah, dari kiri ke kanan, lalu baris demi baris dari bawah ke atas gambar. Format piksel dan implikasinya tercantum di bawah ini:

* Format 1-bit per piksel (1bpp) mendukung 2 warna berbeda, (misalnya: hitam dan putih).
* Format 2-bit per piksel (2bpp) mendukung 4 warna berbeda dan menyimpan 4 piksel per 1 byte, piksel paling kiri berada di dua bit paling signifikan. Setiap nilai piksel adalah indeks 2-bit ke dalam tabel hingga 4 warna.
* Format 4-bit per piksel (4bpp) mendukung 16 warna berbeda dan menyimpan 2 piksel per 1 byte, piksel paling kiri berada di gigitan yang lebih signifikan. Setiap nilai piksel adalah indeks 4-bit ke dalam tabel hingga 16 warna.
* Format 8-bit per piksel (8bpp) mendukung 256 warna berbeda dan menyimpan 1 piksel per 1 byte. Setiap byte adalah indeks ke dalam tabel hingga 256 warna.
* Format 16-bit per piksel (16bpp) mendukung 65536 warna berbeda dan menyimpan 1 piksel per 2-byte KATA. Setiap KATA dapat menentukan sampel alfa, merah, hijau, dan biru dari piksel.
* Format piksel 24-bit (24bpp) mendukung 16.777.216 warna berbeda dan menyimpan 1 nilai piksel per 3 byte. Setiap nilai piksel menentukan sampel piksel merah, hijau, dan biru (8.8.8.0.0 dalam notasi RGBAX). Khususnya, dalam urutan: biru, hijau, dan merah (8 bit per setiap sampel).
* Format 32-bit per piksel (32bpp) mendukung 4.294.967.296 warna berbeda dan menyimpan 1 piksel per DWORD 4-byte. Setiap DWORD dapat menentukan sampel alfa, merah, hijau, dan biru dari piksel.

## Referensi ##

* [Format MetaFile Windows](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Format File BMP](https://en.wikipedia.org/wiki/BMP_file_format)

