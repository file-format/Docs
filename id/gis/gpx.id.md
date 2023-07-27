{
  "date" : "2019-10-11",
  "keywords" :[ "file gpx", "apa itu file gpx", "file", "contoh gpx", "ekstensi file gpx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Format File Pertukaran GPX",
  "description":"Pelajari tentang format file GPX dan API yang dapat membuat dan membuka file GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GPX?

File dengan ekstensi GPX mewakili format GPS Exchange untuk pertukaran data GPS antara aplikasi dan layanan web di internet. Ini adalah format file XML ringan yang berisi data GPS, yaitu titik arah, rute, dan trek untuk diimpor dan di-red oleh beberapa program. Format file GPX terbuka dan didukung oleh berbagai aplikasi dan perangkat GPS. Data GPS dari file tersebut dapat dimuat untuk ditampilkan pada aplikasi pemetaan untuk tujuan geo-spasial.

## Format File GPX ##

File GPX terdiri dari data lokasi lintang dan bujur, nilai elevasi, dan informasi deskriptif lainnya. Data lokasi dinyatakan sebagai derajat desimal dan elevasi dinyatakan dalam meter. Waktu dalam file GPX berada dalam Coordinated Universal Time (UTC) menggunakan format ISO 8601. Manfaat menggunakan file GPX adalah sebagai berikut:

* GPX memungkinkan Anda bertukar data dengan daftar program yang terus bertambah untuk Windows, MacOS, Linux, Palm, dan PocketPC.
* GPX dapat diubah menjadi format file lain menggunakan halaman web sederhana atau program konverter.
* GPX didasarkan pada standar XML, sehingga banyak program baru yang Anda gunakan (Microsoft Excel, misalnya) dapat membaca file GPX.
* GPX memudahkan siapa saja di web untuk mengembangkan fitur baru yang akan langsung berfungsi dengan program favorit Anda.

[Skema GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) menampilkan representasi format file GPX untuk referensi.

### Data Penting ###

Berikut adalah data penting yang merupakan bagian dari file GPX untuk representasi data GPS.

* **Waypoints**: Waypoint adalah koordinat titik WGS84 (GPS) dan mewakili lapisan fitur tipe OGR wkbPoint
* **Rute**: Mewakili lapisan fitur wkwLineString tipe OGR. Ini termasuk daftar titik lintasan, yang merupakan titik arah yang menunjukkan belokan atau titik tahapan yang mengarah ke tujuan
* **Tracks**: Tracks mewakili lapisan fitur tipe OGR wkwMultiLineString. Itu terbuat dari setidaknya satu segmen yang berisi titik arah dalam daftar titik yang diurutkan yang menggambarkan jalur. Ini terdiri dari daftar titik lintasan yang mewakili lintasan GPS berkelanjutan.

### File Contoh GPX ###

File GPX berikut menunjukkan organisasi data GPS dalam file GPX dan dapat memberikan ide bagus tentang konten file GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Referensi ##

* [Format File GPX](https://www.topografix.com/gpx.asp)
* [GPX - Oleh Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

