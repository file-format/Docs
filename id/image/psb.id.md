{
  "date" : "2019-10-11",
  "keywords" :[ "file psb", "format file psb", "apa itu file psb", "file", "contoh psb", "ekstensi file psb", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Format File Gambar Besar Photoshop",
  "description":"Pelajari tentang format file PSB dan API yang dapat membuat dan membuka file PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PSB?
Adobe photoshop menyimpan file dalam dua format. File berukuran 30.000 x 30.000 piksel disimpan dengan ekstensi PSD dan file yang lebih besar dari PSD hingga 300.000 x 300.000 piksel disimpan dengan ekstensi PSB yang dikenal sebagai "Photoshop Big". Lebih khusus lagi, file PSB bisa sebesar 4 EB (lebih dari 4,2 miliar GB) dengan gambar yang memiliki tinggi dan lebar hingga 300.000 piksel. PSD, di sisi lain, dapat berukuran maksimal hingga 2 GB dan dimensi gambar 30.000 piksel.

PSB juga dikenal sebagai ukuran format besar untuk photoshop dan mendukung semua fitur photoshop seperti layer, efek, dan filter.Photoshop dapat mengonversi file PSB menjadi [PSD](/id/image/psd/), [JPG](/id/image/jpeg/) , [PNG](/id/image/png/), [EPS](/id/page-description-language/eps/), [GIF](/id/image/gif/) dan juga format lainnya. Format dokumen besar Photoshop tersedia setelah fitur panel penanganan file dari kotak dialog preferensi Photoshop diaktifkan.

## Informasi Format File ##

Format file Photoshop dibagi menjadi lima bagian utama dengan banyak penanda panjang untuk berpindah antar bagian.

|Format file
---|
|Berkas Tajuk
|Data Mode Warna
| Sumber Gambar
|Lapisan dan Informasi Topeng
|(((
Data Gambar
)))

### Kepala Berkas ###

Header file memiliki panjang tetap 26 byte dan berisi properti dasar gambar.

Tanda Tangan BYTE [4] – Sama dengan '8BPS'.

Versi KATA [2] – Nomor Versi, PSD #1, PSB #2.

BYTE Dicadangkan [6] – Dicadangkan dan selalu nol.

Saluran KATA [2] – Jumlah saluran warna dalam gambar termasuk saluran alfa. Nilainya berkisar dari 1 hingga 56.

Baris PANJANG [4] – Tinggi gambar dalam piksel, PSD 1-30.000, PSB 1-300.000.

LONG Columns [4] – Lebar gambar dalam piksel, PSD 1-30.000, PSB 1-300.000.

Kedalaman KATA [2] – Jumlah bit per saluran. Nilai yang didukung adalah 1,8,16 dan 32.

Mode KATA [2] – Mode Warna file.

#### Deskripsi Mode ####


|Mode|Deskripsi
---|---|
|0|Bitmap (monokrom)
|1|Skala abu-abu
|2|Terindeks
|3|RGB
|4|CMYK
|7|Multisaluran
|8|Duoton (setengah nada)
|9|Laboratorium

### Data Mode Warna ###

Setelah bagian header file, bagian data mode warna mengikuti. Blok dimulai dengan LONG Number yang memberikan panjang blok dalam byte. Struktur data mode warna adalah sebagai berikut:

4 byte – Panjang data warna berikut.

Variabel – Data Warna

Jika nilai kolom mode di bagian header bukan Indexed Color atau duotone, panjang blok akan menjadi 0 dan tidak akan ada data setelah kolom panjang.

Untuk Gambar Berwarna Terindeks, panjangnya akan menjadi 768 byte yang akan berisi 256 palet warna. Untuk duotone, data akan berisi parameter layar dan informasi terkait lainnya.

### Sumber Gambar ###

Mengikuti bagian data mode warna, blok ketiga adalah bagian sumber gambar. Empat byte pertama adalah nomor PANJANG yang menentukan panjang blok diikuti oleh serangkaian blok sumber daya. Struktur blok sumber daya gambar adalah sebagai berikut:

Tipe BYTE [4] – Tanda tangan '8BIM'

WORD ID [2] – ID Sumber Daya Gambar. Ada daftar ID Sumber Daya yang dapat dilihat dari tautan referensi.

Nama BYTE [Variabel] – Nama: String Pascal dengan panjang genap. ** **

Ukuran PANJANG [4] – Ukuran sebenarnya dari data sumber daya yang mengikuti.

Data BYTE [Variabel} – Data sumber daya. Itu empuk untuk membuat ukuran genap.

Beberapa format sumber daya dijelaskan secara singkat di bawah ini:

**Format Sumber Daya Kisi dan Panduan:** Informasi Kisi dan Panduan disimpan di blok sumber daya. Blok sumber daya ini berisi kisi 16 byte dan tajuk panduan diikuti oleh 5 blok byte informasi panduan.

**Format Sumber Daya Gambar Kecil:** Informasi gambar kecil disimpan dalam blok sumber daya gambar untuk tampilan pratinjau yang terdiri dari header 28 byte dan gambar kecil JFIF dalam RGB.

**Format Sumber Daya sampel warna:** Informasi sampel warna disimpan dalam blok sumber daya gambar dengan header 8 byte diikuti dengan blok panjang variabel informasi sampel warna.

### Informasi Layer dan Mask ###

Blok keempat adalah blok informasi layer dan mask dan berisi informasi tentang layer dan mask. Informasi lapisan disimpan terlebih dahulu dan kemudian menutupi informasi.

**Informasi Lapisan:** Informasi lapisan dimulai dengan nilai PANJANG yang menunjukkan panjang informasi lapisan. Setelah itu ada hitungan nilai WORD yang menunjukkan jumlah record layer yang akan diikuti.

[8] – panjang lapisan

[2] – Jumlah Lapisan

[Variabel] – Informasi tentang setiap lapisan.

[Variabel] – Data gambar saluran.** **

**Informasi Topeng:** Struktur topeng memiliki format berikut:


|Struktur Data|Nama Bidang| Keterangan
---|---|---|
|KATA| Hamparan Ruang Warna| (Tidak didokumentasikan)
|BYTE[8]| Komponen Warna| Komponen warna 4x2 byte
|KATA| Opasitas| 0#transparan, 1#buram
|BYTE| Jenis| 0#terbalik, 1#terlindungi, 128#menggunakan nilai tersimpan
|BYTE| bantalan| disetel ke nol

### Data Gambar ###

Bagian terakhir berisi data piksel gambar. Data gambar disimpan sebagai rangkaian urutan dalam bidang yaitu pertama semua data merah, lalu semua data hijau, dll. KATA pada awal setiap baris menunjukkan ukuran dalam byte yang terkait dengan setiap baris pemindaian.

[2] – Metode kompresi:

[Variabel] – Data Gambar dalam urutan planar yaitu RRRR, GGGG, BBBB dll.

Metode Kompresi:

0 – Raw Data Gambar

1 – RLE Dikompresi

2 – Zip tanpa Prediksi

3 – Zip dengan prediksi

## Referensi ##

* [Format File PSB - Oleh Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

