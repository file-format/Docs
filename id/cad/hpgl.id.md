{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Format File", "Buka", "Baca", "Buat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file HPGL dan API yang dapat membuat dan membuka file HPGL.",
  "title" :"Format File HPGL - Belajar dari Pakar Format File!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Apa itu file HPGL?

File HPGFL (Hewlett-Packard Graphics Language) berisi set instruksi untuk kontrol plotter yang dikembangkan oleh HP. Komplotan HP menggunakan file ini untuk menggambar dan mencetak konten vektor dan raster di atas kertas.

### Perintah HPGL

Perintah HPGL terdiri dari yang berikut ini.
* Sebuah bagian perintah dari alfabet dua karakter
* Bagian parameter
* Bagian Terminator

Setiap parameter dalam file harus dipisahkan dengan pemisah jika ada beberapa parameter.

### Contoh Perintah HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Sistem koordinasi

Sistem koordinat terdiri dari indikator pengukuran 2 dimensi untuk menemukan lokasi tertentu. HPGL menggunakan koordinat Plotter dan sistem koordinat pengguna untuk tujuan ini.

#### Sistem Koordinat Plotter

Sistem koordinat ini digunakan untuk memplot gambar berdasarkan pergerakan plotter. Satuan XY tipikal dari pergerakan plotter minimum adalah 0,025mm. Rentang kemungkinan perubahan gambar dengan jenis plotter.

#### Sistem koordinat pengguna

Sistem koordinat yang ditentukan pengguna dapat diatur menggunakan skala dan asal. Ini dikonversi ke koordinat plotter menggunakan perintah IP dan perintah SC. Koordinat sistem plotter digunakan secara default jika konversi ini tidak dilakukan.

## Format File HPGL
File HPGL dalam format ASCII (file teks) dan mulai dengan beberapa perintah penyiapan. Ini mengatur parameter tertentu untuk plotter untuk merencanakan. File HPGL tipikal terlihat sebagai berikut.

|Perintah|Arti
---|---|
|IN;|menginisialisasi, memulai pekerjaan merencanakan|
|IP;|atur titik penskalaan (P1 dan P2) ke posisi defaultnya|
|SP1;|pilih pena 1|
|PU0,0;|lift Pen Up dan pindah ke titik awal untuk tindakan selanjutnya|
|PD100,0,100,100,0,100,0,0;|letakkan Pen Down dan pindah ke lokasi berikut (gambar kotak di sekeliling halaman)|
|PU50,50;|Pena Atas dan pindah ke koordinat X,Y 50,50|
|CI25;|gambar lingkaran dengan jari-jari 25|
|SS;|pilih set karakter standar|
|DT*,1;|setel pembatas teks ke tanda bintang, dan jangan cetak (angka 1, artinya "benar")|
|PU20,80;|angkat pena dan pindah ke 20,80|
|LBHalo Dunia*;|gambar label|

## Referensi
* [HPGL oleh Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Panduan Referensi HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

