{
  "date" : "2019-10-11",
  "keywords" :[ "file tiff", "format file tiff", "apa itu file tiff", "file", "contoh tiff", "ekstensi file tiff", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Format Berkas Gambar",
  "description":"Pelajari tentang format file TIFF dan API yang dapat membuat dan membuka file TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file TIFF?

TIFF atau TIF, Tagged Image File Format, mewakili gambar raster yang dimaksudkan untuk digunakan pada berbagai perangkat yang sesuai dengan standar format file ini. Itu mampu menggambarkan data gambar bilevel, skala abu-abu, warna palet dan penuh warna di beberapa ruang warna. Ini mendukung skema kompresi lossy dan lossless untuk memilih antara ruang dan waktu untuk aplikasi yang menggunakan format tersebut. Formatnya tidak bergantung pada mesin dan bebas dari batasan seperti prosesor, sistem operasi, atau sistem file.

## Sejarah Singkat Format File TIFF

Format file TIFF awalnya dibuat oleh Aldus Corporation pada musim gugur 1986, setelah serangkaian pertemuan dengan berbagai produsen pemindai dan pengembang perangkat lunak. Tujuan utama format file TIFF adalah untuk menyediakan format file gambar pindaian umum untuk semua vendor pemindai desktop. Dimulai dengan dukungan hanya untuk format gambar biner, format tersebut berkembang menjadi dukungan skala abu-abu dan gambar berwarna seiring berjalannya waktu. Versi awal spesifikasi format file TIFF dapat diberi label sebagai Reivision 3.0 karena ada dua rilis draf sebelumnya. Revisi 5.0 utama diterbitkan pada tahun 1988 yang menambahkan dukungan untuk gambar warna palet dan kompresi LZW. Revisi 6.0 format file TIFF diterbitkan pada tahun 1992 setelah itu. Pada tahun 1994, Adobe Systems mengakuisisi Aldus dan spesifikasinya sekarang tersedia dan dikelola oleh Adobe Systems.

## Spesifikasi Format File TIFF

Format file TIFF dapat diperluas dan telah mengalami beberapa revisi yang memungkinkan penyertaan informasi pribadi atau tujuan khusus dalam jumlah yang tidak terbatas. File TIFF dimulai dengan header 8-byte di mana byte diberi nomor dari 0 hingga N. File TIFF terbesar yang mungkin berukuran panjang 2**32 byte. File dimulai dengan header file gambar 8-byte yang menunjuk ke file gambar secara langsung (IFD). IFD berisi informasi tentang gambar serta penunjuk ke data gambar yang sebenarnya.

### Tajuk Berkas TIFF

Header file TIFF 8-byte berisi informasi berikut:

**Byte 0-1:** Urutan byte yang digunakan dalam file. Nilai hukumnya adalah:“II”(4949.H)“MM” (4D4D.H).

Dalam format "II", urutan byte selalu dari byte paling signifikan ke byte paling signifikan, untuk bilangan bulat 16-bit dan 32-bit. Ini disebut urutan byte little-endian. Dalam format "MM", urutan byte selalu dari yang paling signifikan hingga yang paling tidak signifikan, untuk bilangan bulat 16-bit dan 32-bit. Ini disebut urutan byte big-endian.

**Byte 2-3:** Angka acak namun dipilih dengan hati-hati (42) yang selanjutnya mengidentifikasi file sebagai file TIFF. Urutan byte bergantung pada nilai Byte 0-1.

**Byte 4-7:** Offset (dalam byte) IFD pertama. Direktori boleh berada di sembarang lokasi dalam file setelah header tetapi harus dimulai pada batas kata. Secara khusus, Direktori File Gambar dapat mengikuti data gambar yang dijelaskannya. Pembaca harus mengikuti penunjuk ke mana pun petunjuk itu mengarah. Istilah byte offset selalu digunakan dalam dokumen ini untuk merujuk ke lokasi sehubungan dengan awal file TIFF. Byte pertama dari file memiliki offset 0.

### Direktori File Gambar

Sebuah IFD berisi informasi tentang gambar serta penunjuk ke data gambar sebenarnya. Ini terdiri dari hitungan 2-byte dari jumlah entri direktori (yaitu jumlah bidang), diikuti dengan urutan entri bidang 12-byte , diikuti dengan offset 4 byte dari IFD berikutnya (atau 0 jika tidak ada). Harus ada setidaknya 1 IFD dalam file TIFF dan setiap IFD harus memiliki setidaknya satu entri.

#### Entri IFD

Setiap Entri IFD 12-byte dalam format berikut.


|Byte|Deskripsi
---|---|
|0-1|Tag yang mengidentifikasi bidang
|2-3|Jenis kolom
|4-7|Jumlah dari jenis yang ditunjukkan
|8-11|The Value Offset, file offset (dalam byte) dari Nilai untuk field.Nilai diharapkan dimulai pada batas kata; Dengan demikian, Value Offset yang sesuai akan menjadi angka genap. Offset file ini dapat mengarah ke mana saja dalam file, bahkan setelah data gambar

Bidang TIFF adalah entitas logis yang terdiri dari tag TIFF dan nilainya. Konsep logis ini diimplementasikan sebagai Entri IFD, ditambah nilai sebenarnya jika tidak sesuai dengan bagian nilai/offset, 4 byte terakhir dari Entri IFD. Istilah bidang TIFF dan entri IFD dapat dipertukarkan di sebagian besar konteks.

### TIFF Dasar ###

Baseline TIFF adalah inti dari TIFF, hal-hal penting yang harus didukung oleh semua pengembang TIFF arus utama dalam produk mereka. Kesesuaian dengan format TIFF tunduk pada kepatuhan terhadap persyaratan TIFF Dasar. Persyaratan ini didokumentasikan dengan baik dalam dokumen spesifikasi 6.0.

#### Beberapa Gambar Per File ####

Mungkin ada lebih dari satu IFD dalam file TIFF. Setiap IFD mendefinisikan subfile. Salah satu potensi penggunaan subfile adalah untuk menggambarkan gambar terkait, seperti halaman transmisi faksimili. Pembaca TIFF Baseline tidak diharuskan membaca IFD apa pun selain yang pertama.

#### Jenis Gambar ####

Baseline TIFF Image memiliki tipe berikut:

**Bilevel:** Gambar bilevel berisi dua warna—hitam dan putih. TIFF memungkinkan aplikasi untuk menulis data bilevel dalam format putih-nol atau hitam-nol. Bidang yang merekam informasi ini disebut **PhotometricInterpretation**.

* RGB penuh warna

Informasi PhotometricInterpretation untuk gambar Bilevel adalah sebagai berikut:

Tag = 262 (106.H)
Jenis = PENDEK
**Nilai**

|Nilai|Deskripsi|
---|---|
|0|Untuk gambar bilevel dan skala abu-abu: 0 dicitrakan sebagai putih. Nilai maksimum dicitrakan sebagai hitam. Ini adalah nilai normal untuk Kompresi#2|
|1|BlackIsZero. Untuk gambar bilevel dan skala abu-abu: 0 dicitrakan sebagai hitam. Nilai maksimum dicitrakan sebagai putih. Jika nilai ini ditentukan untuk Compression#2, gambar harus ditampilkan dan dicetak terbalik.|

**GrayScale:** Gambar grayscale adalah generalisasi dari gambar bilevel. Gambar bilevel hanya dapat menyimpan data gambar hitam putih, tetapi gambar skala abu-abu juga dapat menyimpan nuansa abu-abu. Untuk mendeskripsikan gambar tersebut, Anda harus menambahkan atau mengubah bidang berikut. Bidang wajib lainnya sama dengan bidang yang diperlukan untuk gambar bilevel. Untuk gambar skala abu-abu, Kompresi #1 atau 32773 (PackBits). Di Baseline TIFF, gambar skala abu-abu dapat disimpan sebagai data yang tidak dikompresi atau dikompresi dengan algoritme PackBits.

Informasi **BitsPerSample** untuk gambar grayscale adalah sebagai berikut:

Tag = 258 (102.H)
Jenis = PENDEK

Jumlah bit per komponen. Nilai yang diizinkan untuk gambar skala abu-abu TIFF Baseline adalah 4 dan 8, memungkinkan 16 atau 256 warna abu-abu yang berbeda.

**Warna Palet:** Gambar berwarna palet mirip dengan gambar skala abu-abu. Mereka masih memiliki satu komponen per piksel, tetapi nilai komponen digunakan sebagai indeks ke dalam tabel pencarian RGB penuh. Untuk mendeskripsikan gambar seperti itu, Anda perlu menambahkan atau mengubah bidang berikut. Bidang wajib lainnya sama dengan bidang untuk gambar skala abu-abu.
Informasi PhotometricInterpretation untuk gambar Palette-Color adalah sebagai berikut:

PhotometricInterpretation = 3 (Palet Color).
ColorMapTag = 320 (140.H)
Jenis = PENDEK
N = 3 * (2 BitPerSample)

Bidang ini menentukan peta warna Merah-Hijau-Biru (sering disebut tabel pencarian) untuk gambar berwarna palet. Dalam gambar berwarna palet, nilai piksel digunakan untuk mengindeks ke dalam tabel pencarian RGB. Misalnya, piksel warna palet yang memiliki nilai 0 akan ditampilkan sesuai dengan triplet Merah, Hijau, Biru ke-0. Dalam Peta Warna TIFF, semua nilai Merah didahulukan, diikuti nilai Hijau, kemudian nilai Biru. Dalam ColorMap, hitam diwakili oleh 0,0,0 dan putih diwakili oleh 65535, 65535, 65535.

**RGB penuh warna:** Dalam gambar RGB, setiap piksel terdiri dari tiga komponen: merah, hijau, dan biru. Tidak ada ColorMap. Untuk menggambarkan gambar RGB, Anda perlu menambah atau mengubah bidang dan nilai berikut. Bidang wajib lainnya sama dengan bidang yang diperlukan untuk gambar berwarna palet.

BitPerSample = 8,8,8. Setiap komponen sedalam 8 bit dalam gambar Baseline TIFF RGB.

PhotometricInterpretation = 2 (RGB) dan tidak ada ColorMap.

Tag = 277 (115.H)
Jenis = PENDEK
Jumlah komponen per piksel. Angka ini adalah 3 untuk gambar RGB, kecuali jika ada sampel tambahan.

## Referensi ##

* [Format File TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

