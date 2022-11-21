{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "file", "ekstensi", "format file", "Lokasi GPS", "Titik arah" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Format Berkas Lokasi GPS",
  "description":"Pelajari tentang format file LOC dan API yang dapat membuat dan membuka file LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Apa itu file LOC?

File dengan ekstensi .loc adalah file lokasi GPS yang berisi lokasi geospasial sebagai titik arah. Waypoint adalah sepasang nilai Lintang-Bujur yang mengacu pada lokasi yang digunakan oleh aplikasi Sistem Informasi Geografis (SIG). Program pemetaan GPS, seperti DeLorme Topo, menggunakan file LOC untuk membaca dan menampilkan informasi yang terkandung dalam file LOC ini sebagai lapisan yang dapat dipilih oleh pengguna akhir. Selain itu, ini digunakan untuk bertukar data GPS antar aplikasi. File LOC dapat dibuka menggunakan aplikasi seperti [TopoGrafix EasyGPS](https://www.easygps.com/) yang menampilkan konten file seperti lapisan dan data yang diplot pada peta di geolokasi masing-masing.

## Format File LOC - Informasi Lebih Lanjut

File LOC memiliki kemiripan dengan file [GPX](/id/gis/gpx/) tetapi disimpan dalam format yang berbeda. Ini disimpan sebagai file [XML](/id/web/xml/) tempat konten titik arah dan informasi terkait dimuat dalam tag terstruktur. Karena XML adalah bahasa umum untuk pertukaran data antara aplikasi yang berbeda, ini memfasilitasi pertukaran data LOC dengan aplikasi lain.

## Format File LOC - Contoh

Berikut ini adalah header dan teks dari salah satu waypoint dari file LOC. Seperti dapat dilihat, informasi header berisi sumber lokasi data. Waypoint berisi informasi seperti `ID` dan data konten terkait yang terkait dengan waypoint. Terakhir, waypoint adalah kumpulan nilai lintang dan bujur dan teks yang terkait dengan waypoint khusus ini.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Referensi

* [EasyGPS Grafis Teratas](https://www.easygps.com/)

