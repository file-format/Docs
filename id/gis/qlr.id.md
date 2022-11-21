{
  "date" : "2019-10-11",
  "keywords" :[ "file qlr", "format file qlr", "apa itu file qlr", "file", "contoh qlr", "ekstensi file qlr", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - File Definisi Lapisan QGIS",
  "description":"Pelajari tentang format file QLR dan API yang dapat membuat dan membuka file QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Apa itu file QLR?

File dengan .qlr adalah file Layer Definition yang berisi pointer ke sumber data layer. Ini merupakan tambahan untuk informasi gaya [QGIS](https://www.qgis.org/en/site/) untuk layer. Memiliki referensi ke semua gaya terkait, file ini digunakan sebagai satu sumber data yang akan digunakan untuk mendapatkan informasi gaya. Dengan menggunakan file QLR, informasi ke sumber data dapat dimasukkan ke dalam file tunggal ini yang dapat dibaca oleh aplikasi lain untuk memuat informasi gaya. File QLR dapat dibuka dengan editor teks apa pun seperti Notepad ++.

## Format File QLR

QLR, mirip dengan [QGS](/id/gis/qgs/), adalah file XML yang berisi pointer ke sumber data lapisan dalam bentuk tag XML. Ini mirip dengan file .lyr ArcGIS. Tag tingkat atas dari file QML seperti yang ditunjukkan pada gambar di bawah ini.

{{< figure src="../qlr.png" title="" >}}

## Referensi

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

