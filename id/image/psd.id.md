{
  "date" : "2019-10-11",
  "keywords" :[ "file psd", "format file psd", "apa itu file psd", "file", "contoh psd", "ekstensi file psd", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Format File Gambar Photoshop",
  "description":"Pelajari tentang format file PSD dan API yang dapat membuat dan membuka file PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PSD?

PSD, Dokumen Photoshop, mewakili format file asli Adobe Photoshop yang digunakan untuk perancangan dan pengembangan grafis. File PSD dapat mencakup lapisan gambar, lapisan penyesuaian, lapisan pelindung, anotasi, informasi file, kata kunci, dan elemen khusus Photoshop lainnya. File Photoshop memiliki ekstensi default sebagai .PSD dan memiliki tinggi dan lebar maksimum 30.000 piksel, dan batas panjang dua gigabyte.

## Spesifikasi Format File PSD ##

Data dalam file PSD disimpan dalam urutan byte big endian. Ini berarti menukar bilangan bulat pendek dan panjang saat membaca atau menulis di platform Windows. Format file Photoshop dibagi menjadi lima bagian utama. Ini memiliki banyak penanda panjang yang dapat digunakan untuk berpindah dari satu bagian ke bagian berikutnya. Penanda panjang biasanya diisi dengan byte untuk dibulatkan ke interval 2 atau 4 byte terdekat. Lima bagian besar tersebut adalah:

* Judul File
* Data Mode Warna
* Sumber Gambar
* Informasi Lapisan dan Topeng
* Data Gambar

Untuk kesesuaian, data harus ditulis ke semua bidang ini di bagian, karena Photoshop mungkin mencoba membaca seluruh bagian. Ini juga menyiratkan bahwa nol ditulis ke bidang yang dilewati saat menulis ke file. Bidang panjang di bagian yang dibatasi panjang harus digunakan untuk memutuskan kapan harus berhenti membaca. Dalam kebanyakan kasus, bidang panjang menunjukkan jumlah byte, bukan catatan, yang mengikuti. Poin-poin berikut perlu diingat saat membaca file.

* Nilai dalam kolom "Panjang" di semua tabel dalam satuan byte.
* Semua nilai yang didefinisikan sebagai string Unicode terdiri dari:
* Bidang dengan panjang 4 byte, mewakili jumlah karakter dalam string (bukan byte).
* String nilai Unicode, dua byte per karakter.

### Kepala Berkas ###

Header file berisi properti dasar gambar.

|Panjang|Deskripsi
---|---|
|4|Signature: selalu sama dengan '8BPS' . Jangan mencoba membaca file jika tanda tangannya tidak cocok dengan nilai ini.
|2|Versi: selalu sama dengan 1. Jangan mencoba membaca berkas jika versi tidak cocok dengan nilai ini. (~*~*PSB~*~* versi 2.)
|6|Dicadangkan: harus nol.
|2|Jumlah saluran dalam gambar, termasuk semua saluran alfa. Kisaran yang didukung adalah 1 hingga 56.
|4|Tinggi gambar dalam piksel. Kisaran yang didukung adalah 1 hingga 30.000.
|4|Lebar gambar dalam piksel. Kisaran yang didukung adalah 1 hingga 30.000.
|2|Kedalaman: jumlah bit per saluran. Nilai yang didukung adalah 1, 8, 16 dan 32.
|2|Mode warna berkas. Nilai yang didukung adalah: Bitmap # 0; Skala abu-abu # 1; Diindeks # 2; RGB #3; CMYK #4; Multisaluran #7; Duonada # 8; Laboratorium #9.

### Bagian Data Mode Warna ###

Bagian data mode warna disusun sebagai berikut:


|Panjang|Deskripsi
---|---|
|4|Panjang data Warna berikut
|variabel|Data warna

Data mode warna hanya tersedia untuk warna yang diindeks dan duotone seperti yang ditentukan oleh bidang mode di bagian File Header. Untuk semua mode lainnya, bagian ini diwakili oleh nilai nol 4-byte. Untuk gambar berwarna yang diindeks, panjangnya adalah 768 dan data warna berisi tabel warna untuk gambar tersebut, dalam urutan yang tidak disisipkan. Untuk gambar Duotone, data warna berisi spesifikasi duotone (yang formatnya tidak didokumentasikan). Aplikasi lain yang membaca file Photoshop dapat memperlakukan gambar duotone sebagai gambar abu-abu, dan menyimpan konten informasi duotone saat membaca dan menulis file.

### Bagian Sumber Daya Gambar ###

Bagian ketiga file berisi sumber daya gambar. Itu dimulai dengan bidang panjang, diikuti oleh serangkaian blok sumber daya.


|Panjang|Deskripsi
---|---|
|4|Panjang bagian sumber daya gambar. Panjangnya mungkin nol.
|Variabel|Sumber Daya Gambar (Blok Sumber Daya Gambar)

Sumber daya gambar digunakan untuk menyimpan data non-piksel yang terkait dengan gambar seperti jalur alat pena. Mereka disebut sebagai blok sumber daya karena menyimpan data yang disimpan di sumber daya Macintosh di versi awal Photoshop. Struktur dasar blok sumber daya gambar adalah seperti yang ditunjukkan di bawah ini:


|Panjang|Deskripsi
---|---|
|4|Tanda tangan: '8BIM'
|2|Identifikasi unik untuk sumber daya. ID sumber daya gambar berisi daftar ID sumber daya yang digunakan oleh Photoshop.
|Variabel|Nama: Pascal string, diisi untuk membuat ukuran genap (nama null terdiri dari dua byte 0)
|4|Ukuran sebenarnya dari data sumber daya yang mengikuti
|Variabel|Data sumber daya, dijelaskan di bagian pada jenis sumber daya individual. Itu empuk untuk membuat ukurannya rata.

Sumber daya gambar menggunakan beberapa nomor ID standar.

### Informasi Layer dan Mask ###

Bagian keempat dari file Photoshop berisi informasi tentang lapisan dan topeng seperti jumlah lapisan, saluran dalam lapisan, rentang campuran, kunci lapisan penyesuaian, lapisan efek, dan parameter topeng. Jika tidak ada lapisan atau topeng, bagian ini diwakili oleh bidang 4-byte yang dikosongkan. Perhatian khusus perlu diberikan pada panjang bagian saat membaca bagian ini karena nilai nol. Susunan bagian Layer dan Mask adalah sebagai berikut:


|Panjang|Deskripsi
---|---|
|4|Panjang bagian informasi layer dan mask. (Panjang PSB adalah 8 byte.)
|Variabel|Info lapisan
|Variabel|Info layer mask global
|Variabel|Serangkaian blok yang ditandai berisi berbagai jenis data.

#### Info Lapisan ####

Tabel berikut menunjukkan organisasi tingkat tinggi dari informasi layer.


|Panjang|Deskripsi
---|---|
|4|Panjang bagian info lapisan, dibulatkan menjadi kelipatan 2. (Panjang PSB adalah 8 byte.)
|2|Jumlah lapisan. Jika berupa angka negatif, nilai absolutnya adalah jumlah lapisan dan saluran alfa pertama berisi data transparansi untuk hasil gabungan.
|Variabel|Informasi tentang setiap lapisan. Lihat Lapisan catatan menjelaskan struktur informasi ini untuk setiap lapisan.
|Variabel|Data gambar saluran. Berisi satu atau lebih rekaman data gambar untuk setiap lapisan. Lapisan berada dalam urutan yang sama seperti pada informasi lapisan

### Data Gambar ###

Data piksel gambar terdapat di bagian Data Gambar pada file. Penataan data pada bagian Data Citra dalam urutan planar yaitu pertama semua data merah, kemudian semua data hijau, dst. Setiap bidang disimpan dalam urutan scan-line, tanpa pad byte, Bagian data gambar disusun dalam format seperti yang ditunjukkan pada tabel berikut.

|Panjang|Deskripsi
---|---|
|2|Metode kompresi: *0 = Data gambar mentah * 1 = RLE mengkompresi data gambar dimulai dengan hitungan byte untuk semua garis pemindaian (baris * saluran), dengan setiap hitungan disimpan sebagai nilai dua byte. Data terkompresi RLE mengikuti, dengan setiap baris pemindaian dikompresi secara terpisah. Kompresi RLE adalah algoritma kompresi yang sama yang digunakan oleh rutin Macintosh ROM PackBits , dan standar TIFF. *2 = ZIP tanpa prediksi *3 = ZIP dengan prediksi.
|Variabel|Data gambar. Urutan planar = RRR GGG BBB, dll.

## Referensi ##

* [Spesifikasi Format File PSD - Oleh Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Format File Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

