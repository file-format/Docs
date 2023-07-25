{
  "date" : "2019-10-11",
  "keywords" :[ "file gml", "apa itu file gml", "file", "contoh gml", "ekstensi file gml", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Format File Bahasa Markup Geografi",
  "description":"Pelajari tentang format file GML dan API yang dapat membuat dan membuka file GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GML?

GML adalah singkatan dari Geography Markup Language yang didasarkan pada spesifikasi XML yang dikembangkan oleh Open Geospatial Consortium (OGC). Format ini digunakan untuk menyimpan fitur data geografis untuk dipertukarkan di antara format file yang berbeda. Ini berfungsi sebagai bahasa pemodelan untuk sistem geografis serta format pertukaran terbuka untuk transaksi geografis di internet.

## Format File GML ##

Seperti kebanyakan tata bahasa berbasis XML, ada dua bagian tata bahasa - skema yang menjelaskan dokumen dan dokumen contoh yang berisi data aktual. Dokumen GML dijelaskan menggunakan Skema GML. Ini memungkinkan pengguna dan pengembang untuk mendeskripsikan kumpulan data geografis umum yang berisi titik, garis, dan poligon. Menggunakan skema aplikasi, pengguna dapat merujuk ke jalan, jalan raya, dan jembatan alih-alih titik, garis, dan poligon.

Perlu diperhatikan bahwa GML tidak boleh diinterpretasikan untuk representasi data spasial pada peta. Representasi konten GML berbeda dari tujuan pembuatan GML. Singkatnya, GML mirip dengan XML yang hanya digunakan untuk menyimpan konten spasial yang dapat digunakan oleh aplikasi pemetaan untuk tujuan tampilan.

### Pembentukan Konten di GML ###

GML merepresentasikan data spasial menggunakan fitur yang merupakan daftar properti dan geometri. Properti memiliki deskripsi nama, jenis, dan nilai. Geometri terdiri dari blok bangunan geometri dasar seperti:

* poin
* baris
* kurva
* sufra dan
* poligon

Versi masa depan GML direncanakan untuk mendukung geometri 3D serta hubungan topologi antar fitur.

Pengkodean GML sudah memungkinkan fitur yang cukup kompleks. Sebuah fitur misalnya dapat terdiri dari fitur lainnya. Sebuah fitur tunggal seperti bandara dengan demikian dapat terdiri dari fitur lain seperti jalur taksi, landasan pacu, gantungan, dan terminal udara. Geometri fitur geografis juga dapat terdiri dari banyak elemen geometri. Dengan demikian, fitur yang kompleks secara geometris dapat terdiri dari campuran jenis geometri termasuk titik, string garis, dan poligon.

### Contoh ###

GML 1.0 dan 2.0 menyandikan objek Poligon, Titik, dan LineString sebagai berikut:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referensi ##

* [Spesifikasi GML](https://www.ogc.org/standard/gml/)
* [GML - Oleh Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

