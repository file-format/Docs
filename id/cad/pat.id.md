{
  "date" : "2020-03-16",
  "keywords" :[ "File PAT", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file PAT dan API yang dapat membuat dan membuka file PAT.",
  "title" :"Format File PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Apa itu file PAT?

File dengan ekstensi .pat adalah file CAD yang digunakan oleh perangkat lunak AutoCAD. Aplikasi yang dapat membuka file PAT menggunakan pola penetasan yang disimpan dalam file tersebut mendapatkan informasi tentang tekstur/isi suatu area. Pola yang terkandung memberikan informasi tentang tampilan material pada objek yang digambar. File PAT dapat dibuka di aplikasi seperti Autodesk AutoCAD, CorelDRAW Graphics Suite, dan Ketron Software. File PAT dapat dikonversi ke format gambar yang berbeda seperti JPG, PNG, BMP, dll.

## Format File PAT

File PAT ditulis dalam format teks biasa dan dapat dibuka di editor teks apa pun. Pola penetasan dalam file ini berbasis vektor dan mengikuti sintaks yang digariskan oleh dokumentasi AutoCAD.

Semua pola dimulai dari titik 0,0, pola dihitung untuk menutupi batas penetasan.

### Definisi Pola

Semua definisi pola terdiri dari bidang-bidang berikut:
* Terkemuka '\*'
* Nama - Nama tidak boleh memiliki spasi, tanda baca, tanda kurung, atau garis miring.
* Sebuah deskripsi

Format standar untuk pola penetasan adalah `<\*><name> <, keterangan>`. Nama dan deskripsi dipisahkan dengan koma dan panjang deskripsi tidak boleh melebihi delapan puluh karakter. Pola penetasan ditentukan setelah informasi ini.

### Contoh Pola Penetasan
Berikut adalah contoh pola persegi
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Contoh lain yang menunjukkan pola jajaran genjang adalah sebagai berikut.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referensi ##

* [Pola Hash oleh Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

