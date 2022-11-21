{
  "date" : "2020-03-16",
  "keywords" :[ "Berkas STL", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file STL dan API yang dapat membuat dan membuka file STL.",
  "title" :"Format Berkas STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu berkas STL?

STL, singkatan dari stereolihrography, adalah format file yang dapat dipertukarkan yang mewakili geometri permukaan 3 dimensi. Format file menemukan penggunaannya di beberapa bidang seperti pembuatan prototipe cepat, pencetakan 3D, dan manufaktur dengan bantuan komputer. Ini mewakili permukaan sebagai rangkaian segitiga kecil, yang dikenal sebagai faset, di mana setiap faset dijelaskan oleh arah tegak lurus dan tiga titik yang mewakili simpul segitiga. Data yang dihasilkan digunakan oleh aplikasi untuk menentukan penampang bentuk 3D yang akan dibangun oleh fabber. Tidak ada informasi yang tersedia dalam format file STL untuk representasi warna, tekstur, atau atribut model [CAD](/id/cad/) umum lainnya.

## Sejarah Singkat ##

Pengembangan format file STL dimulai pada tahun 1987. Ini dikembangkan oleh Sistem 3D untuk penggunaannya dalam printer 3D komersial. Versi format file STL yang direvisi, dikenal sebagai STL 2.0, diusulkan pada tahun 2009 dengan pembaruan format file.

## Spesifikasi Format File ##

File STL mewakili geometri permukaan menggunakan faset. Faset menentukan permukaan objek 3D dan secara unik diidentifikasi oleh satuan normal, yang merupakan garis tegak lurus segitiga dengan panjang 1,0, dan dengan tiga simpul. Ada total 12 angka yang disimpan untuk setiap faset sebagai Normal dan setiap simpul masing-masing ditentukan oleh tiga koordinat. File StL tidak berisi informasi skala apa pun; koordinat berada di unit sewenang-wenang.

Spesifikasi format file STL dapat dilihat dari dua aspek berikut.

### Orientasi faset ###

Orientasi faset ditentukan oleh arah unit normal dan urutan simpul yang terdaftar. Orientasi faset ditentukan dalam dua cara sebagai berikut:

* Arah normalnya adalah ke luar
* Verteks terdaftar dalam urutan berlawanan arah jarum jam dari luar, mengikuti aturan tangan kanan.

### Aturan Simpul ke Simpul ###

Menurut aturan ini, setiap segitiga berbagi dua simpul dengan masing-masing segitiga yang berdekatan. Dengan demikian, simpul dari satu segitiga tidak dapat terletak di sisi segitiga lain.

## Format File ##

STL tersedia dalam ASCII serta representasi Biner untuk format file yang ringkas.

### Format ASCII STL ###

Format file STL versi ASCII ditulis dalam ASCII biasa. Namun, karena ukurannya yang besar, format file tersebut tidak dipilih sebagai format yang lebih disukai untuk digunakan. Sintaks file ASCII STL adalah sebagai berikut:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Kata-kata wajah tebal mewakili kata kunci yang harus selalu huruf kecil. Simbol dalam huruf miring adalah variabel yang harus diganti dengan nilai yang ditentukan pengguna. Data numerik dalam garis **faset normal** dan **vertex** adalah pelampung presisi tunggal, misalnya, 1,23456E+789. Koordinat **faset normal** mungkin memiliki tanda minus di depan; koordinat **vertex** mungkin tidak.

### Format Biner STL ###

Format biner menggunakan integer IEEE dan representasi numerik floating point. Format file direpresentasikan sebagai berikut:

|Lapangan|Info|
---|---|
|Tajuk|80 karakter|
|Jumlah Segitiga|4-byte little endian unsigned integer|
|Data untuk setiap segitiga|12 bilangan floating point 32-bit|

Tampilan yang lebih rumit dari format file adalah seperti yang ditunjukkan di bawah ini.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referensi ##

* [Format STL](http://www.fabbers.com/tech/STL_Format)
* [STL - oleh Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

