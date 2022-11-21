{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "file vdw", "format file vdw", "jenis file vdw", "file", "ketik", "apa itu file vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Format File Layanan Grafis Visio",
  "description":"Pelajari tentang format file VDW dan API yang dapat membuat dan membuka file VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}
## Apa itu file VDW?
VDW adalah format file Layanan Grafik Visio yang menentukan aliran dan penyimpanan yang diperlukan untuk merender gambar Web. Gambar web adalah kumpulan halaman gambar, bentuk, font, gambar, koneksi data, dan informasi pembaruan diagram yang dapat dirender sebagai gambar vektor atau raster. File VDW juga dapat dibuka di Microsoft Visio, tetapi utamanya disimpan untuk digunakan di web. Microsoft Visio menawarkan kemampuan untuk mengonversi file Visio ke beberapa format file yang berbeda termasuk [PNG](/id/Image/PNG/), [BMP](/id/Image/BMP/), [PDF](/id/pdf/), dan lainnya.

## **VDW** Format Berkas #

Spesifikasi teknis format file VDW tersedia online oleh [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) dan dapat dirujuk oleh pengembang untuk membuat aplikasi. Dokumen teknis menjelaskan data yang terkandung dalam file gabungan yang berisi penyimpanan dan aliran. Representasi Gambar Web dimungkinkan melalui aliran, bernama VisioServerData, melalui arsip ZIP. Bagian ShapGraphic XML dalam arsip menjelaskan elemen grafis yang ditampilkan dalam gambar Web dan diekspresikan dalam Extensible Application Markup Language (XAML). Kumpulan bagian XML dalam arsip ZIP menjelaskan koneksi data gambar Web, informasi tentang bentuknya, dan logika pembaruan diagram. Bagian-bagian ini dinyatakan sebagai XML. Bagian DataGraphic XML menjelaskan properti yang dihitung ulang yang akan dievaluasi setelah data di gambar Web di-refresh dari sumber data. Item tambahan dalam arsip ZIP berisi informasi untuk font dan gambar yang digunakan dalam gambar Web.

|![Kemungkinan Implementasi File](/id/web/vdw.png "Kemungkinan Implementasi File")

## Referensi ##

* [[MS-VGSFF]: Format File Layanan Grafik Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

