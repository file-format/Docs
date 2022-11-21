{
  "date" : "2019-10-11",
  "keywords" :[ "file qgs", "format file qgs", "apa itu file qgs", "file", "contoh qgs", "ekstensi file qgs", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Format File Proyek QGIS",
  "description":"Pelajari tentang format file QGS dan API yang dapat membuat dan membuka file QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file QGS?

File dengan ekstensi .qgs adalah file proyek yang dibuat dengan [QGIS](https://www.qgis.org/en/site/), yang merupakan aplikasi GIS lintas platform sumber terbuka. Semua pengaturan proyek seperti properti lapisan dan data tambahan untuk proyek tersebut. Itu dibuat ketika proyek peta disimpan ke disk. Ini sebenarnya adalah file konfigurasi yang menyimpan informasi seperti penunjuk ke data GIS, informasi gaya tentang lapisan, dan judul proyek. File QGS dapat dibuka dengan perangkat lunak QGIS yang tersedia secara gratis untuk diunduh.

## Format File QGS

File QGS dalam format [XML](/id/web/xml/) dan menyimpan data proyek sebagai tag XML. File QGS berisi informasi seperti:

* Judul Proyek
* proyek CRS
* pohon lapisan
* pengaturan gertakan
* hubungan
* luas kanvas peta
* model proyek
* legenda
* dermaga tampilan peta (2D dan 3D)
* lapisan dengan tautan ke kumpulan data yang mendasari (sumber data) dan properti lapisan lainnya termasuk jangkauan, SRS, gabungan, gaya, perender, mode campuran, opasitas, dan lainnya.
* properti proyek

### Tag XML Tingkat Atas QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Tag Lapisan Proyek Tingkat Atas yang Diperluas

{{< figure src="../qgstoplevel.png" title="" >}}

## Referensi

* [QGIS](https://www.qgis.org/en/site/)

