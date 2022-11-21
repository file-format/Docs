{
  "date" : "2019-10-11",
  "keywords" :[ "file kmz", "apa itu file kmz", "file", "contoh kmz", "ekstensi file kmz", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Format File Zip KML",
  "description":"Pelajari tentang format file KMZ dan API yang dapat membuat dan membuka file KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file KMZ?

File KMZ (KML Zipped) adalah representasi dari file zip [KML](/id/gis/kml/) yang berisi informasi geospasial yang dapat dilihat dalam aplikasi GIS seperti Google Earth. Informasi tentang penanda letak ditampilkan dalam file sebagai garis lintang dan garis bujur bersama dengan nama ubahsuaian. File KMZ paket tunggal dapat dibagikan dengan pengguna lain dengan mudah. File KMZ dapat menyertakan data model 3D juga untuk representasi geo model. File KMZ dapat dibuka di Google Maps dengan menyimpan file tersebut ke lokasi online, lalu mengetikkan URL di kotak Pencarian Google Maps.

## Struktur File ##

Isi file MKZ terdiri dari file KML utama dan nol atau lebih file terkait. Itu dapat diekstraksi menggunakan utilitas dekompresi standar seperti WinZIP. Format file KMZ juga dikompres menjadi arsip dengan rasio kompresi 10:1. Anda dapat mengekspor data dari Google Earth seperti aplikasi langsung ke format file KMZ. File KML utama bernama **doc.kml**. Saat mengemas file KMZ, lebih dari satu file KML dapat ditambahkan ke dalamnya, tetapi ini tidak akan bermanfaat karena Google Earth mencari file KML pertama saat membuka file KMZ dan membacanya. Itu mengabaikan file KML lebih lanjut yang ditemukan di arsip. Untuk memastikan file KML yang diinginkan dibaca oleh Google Earth, disarankan hanya satu file KML yang ditempatkan di dalam file KMZ.

Gambar, model, tekstur, file suara, dan sumber daya lain yang direferensikan dalam file doc.kml ditempatkan di subfolder lain di dalam folder utama. Ini mungkin melibatkan beberapa kerumitan juga tergantung pada jumlah file pendukung. Tautan ke sumber daya konstituen ini dapat berupa referensi relatif atau melalui referensi absolut.

### Referensi Relatif ###

Saat sumber daya ditempatkan di samping doc.kml utama di dalam sub-folder di dalam folder utama, referensi relatif dapat mengarah ke file pendukung ini seperti yang ditampilkan dalam contoh berikut (hanya untuk ikon).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Referensi Mutlak ###

Sumber daya dapat direferensikan secara mutlak juga. Referensi absolut berisi URL lengkap untuk file tertaut. Saat file diposting di server pusat, referensi absolut memastikan bahwa ini tetap tidak ambigu dibandingkan dengan referensi relatif. File lokal tidak disarankan untuk direferensikan secara mutlak karena tautan ini akan terputus saat file dipindahkan ke sistem baru. Contoh referensi absolut adalah sebagai berikut:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Lihat juga ##

* [GeoJSON](/id/gis/geojson/)

## Referensi ##

* [File Google Earth dan KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

