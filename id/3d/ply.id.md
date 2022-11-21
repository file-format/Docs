{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "file", "ekstensi", "format", "format file 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file PLY dan API yang dapat membuat dan membuka file PLY.",
  "title" :"PLY - Format File 3D Poligon",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PLY?

PLY, Polygon File Format, mewakili format file 3D yang menyimpan objek grafis yang dideskripsikan sebagai kumpulan poligon. Tujuan dari format file ini adalah untuk membuat tipe file yang sederhana dan mudah yang cukup umum untuk berguna untuk berbagai model. Format file PLY hadir sebagai ASCII serta format Biner untuk penyimpanan yang ringkas dan untuk penyimpanan dan pemuatan yang cepat. Format file digunakan oleh berbagai aplikasi yang mendukung pembacaan file 3D.

Objek dalam format PLY dijelaskan oleh kumpulan simpul, wajah, dan elemen lainnya, bersama dengan properti seperti warna dan arah normal yang dapat dilampirkan ke elemen tersebut. Properti lain yang juga dapat disimpan dengan objek meliputi:

* Permukaan normal
* koordinat tekstur
* transparansi
* rentang kepercayaan data
* properti untuk bagian depan dan belakang poligon

Objek yang diwakili oleh format PLY dapat berupa hasil dari berbagai sumber seperti objek yang didigitalkan dengan tangan, objek poligon dari aplikasi pemodelan, data jangkauan, segitiga dari kubus berbaris, data terrain dan model radiositas.

## Sejarah Singkat

Format PLY dikembangkan pada tahun 1990-an oleh Greg Turk dan yang lainnya di lab grafik Stanford dan itulah mengapa ia juga dikenal sebagai Stanford Triangle Format. Format file memiliki versi 1.0 sejak saat itu dan tidak ada modifikasi lebih lanjut yang dilakukan.

## Format File PLY

Objek PLY sederhana terdiri dari kumpulan elemen untuk representasi objek. Ini terdiri dari daftar (x,y,z) tiga kali lipat dari simpul dan daftar wajah yang sebenarnya indeks ke dalam daftar simpul. Simpul dan wajah adalah dua contoh elemen dan sebagian besar file PLY terdiri dari dua elemen ini. Properti baru juga dapat dibuat dan dilampirkan ke elemen objek, tetapi ini harus ditambahkan sedemikian rupa sehingga program lama tidak rusak saat properti baru ini ditemukan. Properti seperti itu dapat dibuang dengan membaca aplikasi juga. Selain itu, elemen baru dapat dibuat dan properti juga dapat ditentukan dengan elemen ini.

### Struktur Berkas

Struktur file dari format file PLY adalah sebagai berikut:

|Lapangan
---|
|Berkas Tajuk
| Daftar Vertex
| Daftar Wajah
|Daftar elemen lainnya

#### Contoh Struktur

Kami akan menggunakan contoh berikut di bawah ini dalam diskusi kami selanjutnya untuk berbagai bagian dari format file PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Kepala Berkas

Header format file PLY terdiri dari teks ASCII untuk format ASCII dan biner. Awal dan akhir bagian header diidentifikasi dengan kata kunci ply dan end-header. Awal header memiliki kata ajaib ply yang digunakan untuk mengenali format file PLY oleh pembaca. Baris berikutnya menunjukkan nomor versi untuk file ini. Komentar dalam format file PLY dimulai dengan kata kunci komentar di awal setiap baris komentar.

#### Kata Kunci Elemen

Kata kunci elemen kemudian memberi tahu apa yang ada di dalam file. Ini diikuti oleh properti untuk tipe elemen tertentu di mana setiap properti memiliki tipe dan urutan properti yang ditentukan seperti yang ditunjukkan di bawah ini:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Dalam contoh khusus ini, elemen simpul spesifik memiliki 3 properti bertipe float dengan urutannya ditentukan.

#### Tipe Tipe Data

Ada dua jenis tipe data yang mungkin dimiliki properti.

`Scalar`: Tipe data skalar adalah seperti yang ditunjukkan di bawah ini:

|#Nama|#Jenis|#Jumlah Byte
|karakter|karakter|1
|uchar|karakter yang tidak ditandatangani|1
|pendek|bilangan bulat pendek|2
|ushort|bilangan bulat pendek tak bertanda|2
|int|Integer|4
|uint|bilangan bulat tak bertanda|4
|float|pelampung presisi tunggal|4
|ganda|float presisi ganda|8

`Daftar`: Ada bentuk khusus dari definisi properti yang menggunakan tipe data daftar. Contohnya adalah dari file kubus di atas:

`daftar properti uchar int vertex_index`

Ini berarti bahwa properti "vertex_index" pertama berisi karakter unsigned yang memberi tahu berapa banyak indeks yang dikandung properti, diikuti oleh daftar yang berisi banyak bilangan bulat. Setiap bilangan bulat dalam daftar panjang variabel ini adalah indeks ke simpul.

## Referensi ##

* [Format File PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - Oleh Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

