{
  "date" : "2019-10-11",
  "keywords" :[ "file xpm", "format file xpm", "apa itu file xpm", "file", "contoh xpm", "ekstensi file xpm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File XPM - X PixMap",
  "description":"Pelajari tentang format file XPM dan API yang dapat membuat dan membuka file XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file XPM?

File dengan ekstensi .xpm adalah format file gambar yang digunakan oleh Sistem X Windows. Ini mendukung piksel transparan dan biasanya menargetkan pembuatan ikon pixmaps. Ini mendukung data monokrom, skala gra, dan pixmap warna. Ini dirancang untuk dapat diedit dengan tangan dan dapat dimasukkan dalam kode [C](/id/programming/c/). Untuk tujuan ini, file XPM dalam format file teks biasa dan mengikuti sintaks bahasa pemrograman C. File XPM dapat dibuka dengan berbagai aplikasi tampilan gambar seperti
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView, dan Canvas X.

## Format File XPM

Format file XPM menggunakan sintaks C agar ini terintegrasi dalam program C dan C++. Ini terdiri dari enam bagian berbeda berikut.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Bagian sebenarnya adalah array dari string sebagai berikut.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Berikut rincian dari masing-masing bagian.

`<Values> ` - Bagian ini adalah string yang berisi empat atau enam bilangan bulat yang berada di basis 10 dan sesuai dengan:

* lebar dan tinggi pixmap
* jumlah Warna
* jumlah karakter per piksel
* koordinat hotspot opsional dan tag XPMEXT

`<Colors> ` - Bagian ini berisi string sebanyak warna. Setiap string adalah sebagai berikut:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Bagian ini terdiri dari<height> string dan<width> \*<chars_per_pixel> karakter. Setiap<chars_per_pixel> string panjang harus menjadi salah satu grup yang ditentukan sebelumnya di<Colors> bagian.

`<Extension> ` - Bagian ekstensi harus diberi label, jika tidak kosong, di<Values> bagian. Ini mungkin terdiri dari beberapa<Extension> subbagian yang mungkin dari dua jenis berikut:

* satu string yang berdiri sendiri terdiri sebagai berikut: XPMEXT<extension-name><extension-data>
* atau blok yang disusun oleh beberapa string: XPMEXT<extension-name><related extension-data composed of several strings>

## Referensi

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Panduan XPM](http://www.xfree86.org/current/xpm.pdf)

