{
  "date" : "2019-10-11",
  "keywords" :[ "fișier gpx", "ce este un fișier gpx", "fișier", "exemplu gpx", "extensie fișier gpx", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Format de fișier GPX Exchange",
  "description":"Aflați despre formatul de fișier GPX și despre API-urile care pot crea și deschide fișiere GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GPX?

Fișierele cu extensia GPX reprezintă formatul de schimb GPS pentru schimbul de date GPS între aplicații și servicii web de pe internet. Este un format de fișier XML ușor, care conține date GPS, adică puncte de referință, rute și trasee care urmează să fie importate și roșii de mai multe programe. Formatul de fișier GPX este deschis și este acceptat de o varietate de aplicații și dispozitive GPS. Datele GPS din astfel de fișiere pot fi încărcate pentru a fi afișate în aplicațiile de cartografiere în scopuri geo-spațiale.

## Format de fișier GPX ##

Un fișier GPX constă din date despre locație de latitudine și longitudine, valori de altitudine și alte posibile alte informații descriptive. Datele de locație sunt exprimate în grade zecimale, iar altitudinea este exprimată în metri. Ora dintr-un fișier GPX este în Ora universală coordonată (UTC) folosind formatul ISO 8601. Beneficiile utilizării unui fișier GPX sunt următoarele:

* GPX vă permite să faceți schimb de date cu o listă tot mai mare de programe pentru Windows, MacOS, Linux, Palm și PocketPC.
* GPX poate fi transformat în alte formate de fișiere folosind o pagină web simplă sau un program de conversie.
* GPX se bazează pe standardul XML, astfel încât multe dintre programele noi pe care le utilizați (Microsoft Excel, de exemplu) pot citi fișiere GPX.
* GPX facilitează pentru oricine de pe web să dezvolte noi funcții care vor funcționa instantaneu cu programele tale preferate.

[Schema GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) arată reprezentarea formatului de fișier GPX pentru referință.

### Date esențiale ###

Următoarele sunt date esențiale care fac parte dintr-un fișier GPX pentru reprezentarea datelor GPS.

* **Waypoints**: un waypoint este coordonatele WGS84 (GPS) ale unui punct și reprezintă un strat de caracteristici de tip OGR wkbPoint
* **Rute**: reprezintă un strat de caracteristici de tip OGR wkbLineString. Include o listă de puncte de traseu, care sunt puncte de trecere care arată o viraj sau puncte de etapă care duc la o destinație
* **Tracks**: Tracks reprezintă stratul de caracteristici de tip OGR wkbMultiLineString. Este format din cel puțin un segment care conține puncte de trecere într-o listă ordonată de puncte care descriu o cale. Acesta constă dintr-o listă de puncte de urmărire care reprezintă un traseu GPS continuu.

### Fișier exemplu GPX ###

Următorul fișier GPX arată organizarea datelor GPS într-un fișier GPX și poate oferi o idee bună despre conținutul unui fișier GPX.

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

## Referințe ##

* [Format fișier GPX](http://www.topografix.com/gpx.asp)
* [GPX - Prin Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

