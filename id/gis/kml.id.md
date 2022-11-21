{
  "date" : "2019-10-11",
  "keywords" :[ "file kml", "apa itu file kml", "file", "contoh kml", "ekstensi file kml", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Bahasa Markup Lubang Kunci",
  "description":"Pelajari tentang format file KML dan API yang dapat membuat dan membuka file KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file KML?

KML, Keyhole Markup Language) berisi informasi geospasial dalam notasi XML. File yang disimpan sebagai KML dapat dibuka di aplikasi Sistem Informasi Geografis (SIG) asalkan mendukungnya. Banyak aplikasi sudah mulai memberikan dukungan untuk format file KML setelah diadopsi sebagai standar internasional. KML menggunakan struktur berbasis tag dengan elemen dan atribut bersarang. Semua tag peka huruf besar/kecil dan urutan tag ini, sesuai Referensi [KML](https://developers.google.com/kml/documentation/kmlreference), penting untuk diikuti.

## Sejarah Singkat ##

KML awalnya dikembangkan untuk digunakan dengan Google Earth yang awalnya dikenal sebagai Keyhole Earth Viewer. KLM diadopsi sebagai standar internasional pada tahun 2008 oleh Open Geospatial Consortium pada tahun 2008. Karena formatnya dikembangkan untuk digunakan dengan Google Earth, KLM menjadi yang pertama untuk melihat dan mengedit file KML. Dengan berlalunya waktu, sekarang semakin banyak proyek yang menyediakan dukungan untuk format file KML termasuk beberapa API dalam berbagai bahasa.

## Spesifikasi Format File KML ##

Referensi KML adalah panduan lengkap untuk merujuk agar memiliki spesifikasi format file lengkap. File KML standar terdiri dari:

* Tanda letak
* HTML deskriptif dalam Tanda Letak
* Hamparan Tanah
* Jalur
* Poligon

Selain itu, file KML versi lanjutan dapat memiliki:

* Gaya untuk Geometri
* Gaya untuk Ikon yang Disorot
* Hamparan Layar
* Tautan Jaringan

Setiap elemen KML memiliki informasi lat-long yang menempatkan secara geografis informasi yang ada dalam file. Namun, bisa juga ada parameter tambahan seperti arah, ketinggian, dan kemiringan.

### Penanda Tempat ###

Ini digunakan untuk mewakili posisi di permukaan bumi dan diidentifikasi oleh<Point> elemen. Berikut adalah contoh bagaimana tanda letak direpresentasikan dalam file KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML deskriptif dalam Tanda Letak ###

Informasi tambahan dapat diasosiasikan dengan tanda letak yang semakin menyempurnakan representasi tanda letak. Informasi tersebut mencakup tautan, ukuran font, gaya, dan warna. Selain itu, ini juga menyertakan perataan teks dan tabel untuk menjadi bagian dari tanda letak.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Hamparan Tanah ###

Ini mewakili pelapisan gambar ke permukaan bumi. Itu<icon> elment berisi link ke file gambar overlay.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Jalur ###

Jalan diwakili oleh<LineString> elemen yang merupakan kumpulan pasangan lat-long. Dengan menggunakan ini, berbagai jenis jalur dapat dibuat di Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Referensi Spasial di File KML ##

Informasi yang terkandung dalam file Geospasial tentang Geo-Locations dapat memiliki arti yang berbeda tanpa informasi referensi spasial. Secara default, referensi spasial file KML ditentukan oleh Sistem Geodesi Dunia tahun 1984, WGS84.

## Referensi ##

* [Referensi KML](https://developers.google.com/kml/documentation/kmlreference)
* [Tutorial Pengembang Google untuk KML](https://developers.google.com/kml/documentation/kml_tut)
* [Format File KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

