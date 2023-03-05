{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File TCX- File XML Pusat Pelatihan",
  "description":"Pelajari tentang format file TCX dan API yang dapat membuat dan membuka file TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Apa itu file TCX?

File TCX (Training Center XML) adalah format pertukaran data yang digunakan untuk berbagi data antar perangkat kebugaran. Itu diperkenalkan pada tahun 2008 dengan produk Pusat Pelatihan Garmin. Data olahraga seperti detak jantung, irama lari, irama sepeda, kalori, dan waktu putaran disimpan dalam format [XML](/id/web/xml/) di dalam file TCX. Selain itu, data ringkasan tentang trek olahraga juga disertakan dalam file TCX. File TCX mirip dengan file [FIT](/id/gis/fit/) yang dibuat dengan perangkat wearable olahraga Garmin.

## Format File TCX - Informasi lebih lanjut

File TCX disimpan ke disk sebagai file XML dengan setiap rekaman disimpan sebagai aktivitas. Suatu aktivitas terdiri dari semua data latihan seperti waktu, waktu putaran, Id, detak jantung, intensitas, irama, dan informasi trek yang berisi pasangan posisi beserta stempel waktu untuk posisi bujur-latar yang serupa dengan [GPX](/id/gis/gpx/) file.

### Versi Format File TCX

Ada dua versi format ini dengan skema XML mereka sendiri yang dihosting oleh Garmin. Berikut adalah beberapa di antaranya:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protokol Data TCX

Versi cepat format TCX XML tersedia di Github sebagai [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referensi ##

* [XML Pusat Pelatihan](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Penampil TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

