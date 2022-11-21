{
  "date" : "2019-10-11",
  "keywords" :[ "file geojson", "apa itu file geojson", "file", "contoh geojson", "ekstensi file geojson", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Format File Geografis berbasis JSON",
  "description":"Pelajari tentang format file GeoJSON dan API yang dapat membuat dan membuka file GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GeoJSON?

GeoJSON adalah format berbasis JSON yang dirancang untuk mewakili fitur geografis dengan atribut non-spasialnya. Format ini mendefinisikan objek JSON (JavaScript Object Notation) yang berbeda dan mode penggabungannya. Format JSON mewakili informasi kolektif tentang fitur Geografis, luasan spasial, dan propertinya. Objek file ini dapat menunjukkan geometri (Point, LineString, Polygon), fitur atau kumpulan fitur. Fitur mencerminkan alamat dan tempat sebagai jalan titik, jalan utama dan perbatasan sebagai string garis dan negara, provinsi, dan wilayah daratan sebagai poligon. Dengan menggunakan GeoJSON, aplikasi perutean dan navigasi seluler yang berbeda dapat menunjukkan jangkauan layanan mereka. Perpanjangan GeoJSON adalah TopoJSON yang ukurannya lebih kecil dan mengkodekan topologi geospasial.

## Sejarah Singkat ##

Gugus Tugas Teknik Internet (IETF), bekerja sama dengan penulis format, membentuk [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) untuk merilis GeoJSON pada April 2015. Menggantikan 2008 Spesifikasi GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), spesifikasi standar baru dari format GeoJSON yang dipublikasikan pada Agustus 2016.

## Format File GeoJSON ##

### Koordinat ###

Koordinat adalah elemen dasar dari setiap data geografis. Ini adalah dimensi tunggal (Bujur, lintang) yang mewakili satu angka (format desimal) dan terkadang merekam koordinat ketinggian juga. Waktu juga merupakan dimensi, tetapi kerumitannya membuat sulit untuk merekamnya sebagai koordinat. Koordinat di kedua JSON GeoJSON diformat seperti angka.

### Posisi ###

Susunan koordinat yang terurut mewakili [posisi](http://geojson.org/geojson-spec.html#positions). Ini adalah satuan terkecil yang dapat menunjukkan suatu titik di bumi.

`[Bujur, lintang, elevasi]`

Sebelum rilis spesifikasi saat ini, GeoJSON diizinkan merekam tiga koordinat per posisi tetapi tidak diizinkan oleh spesifikasi baru.

### Geometri ###

Geometri adalah bentuk sederhana (titik, kurva, dan permukaan) di GeoJSON yang terdiri dari tipe dan kumpulan koordinat. Titik adalah geometri paling sederhana yang mewakili satu posisi

`{ "type": "Titik", "koordinat": [0, 0] }`

### Baris Baris ###

Setidaknya dua tempat yang terhubung digunakan untuk mewakili garis.

`{ "ketik": "LineString", "koordinat": [[10, 30], [10, 10]] }`

String titik dan garis adalah dua kategori geometri yang paling sederhana. Kedua jenis geometri tidak mengganggu banyak aturan geometris. Sebuah titik dapat direpresentasikan di suatu tempat di mana saja, dan sebuah garis dapat memiliki lebih dari satu titik, bahkan jika titik-titik tersebut bersilangan sendiri.

### Poligon ###

Geometri GeoJSON tampak jauh lebih kompleks dalam Poligon. Poligon memiliki area dalam & luar dan dapat memiliki lubang di dalamnya.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

Dibandingkan dengan LineStrings, dalam poligon, daftar koordinat satu tingkat lebih bersarang dan dapat memiliki potongan seperti donat.

### Tingkat Koordinat ###

Dalam format GeoJSON, untuk properti koordinat, terdapat empat tingkat kedalaman.

### Fitur ###

Geometri adalah bagian sentral dari GeoJSON, oleh karena itu, data dunia nyata lebih dari sekadar bentuk sederhana ini yang memiliki identitas dan atribut. Fitur merekam geometri serta propertinya.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Properti fitur dapat berupa jenis objek [JSON](http://json.org/) yang berisi pemetaan nilai kunci dengan kedalaman tunggal.

### Koleksi Fitur ###

Di tingkat atas file GeoJSON, FeatureCollectionadalah hal paling umum yang terlihat seperti:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Banyak paket perangkat lunak pemetaan dan GIS yang mendukung GeoJSON termasuk perangkat lunak GeoDjango, OpenLayers, dan Geoforge. Ini juga kompatibel dengan PostGIS dan Mapnik. Layanan API dari peta Google, yahoo dan Bing juga mendukung GeoJSON.

## Referensi ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Oleh Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

