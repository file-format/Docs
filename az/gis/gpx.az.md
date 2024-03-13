{
  "date": "2019-10-11",
  "keywords": [
"gpx faylı",
"gpx faylı nədir",
"fayl",
"gpx nümunəsi",
"gpx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX - GPX Exchange fayl formatı",
  "description": "GPX fayl formatı və GPX faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-azx"
}
},
  "lastmod": "2019-09-10"
}

## GPX faylı nədir?

GPX uzantısı olan fayllar internetdəki tətbiqlər və veb xidmətləri arasında GPS məlumatlarının mübadiləsi üçün GPS Mübadilə formatını təmsil edir. Bu, GPS məlumatlarını, yəni keçid nöqtələrini, marşrutları və çoxsaylı proqramlar tərəfindən idxal ediləcək və qırmızı yolları ehtiva edən yüngül çəkili XML fayl formatıdır. GPX fayl formatı açıqdır və müxtəlif proqramlar və GPS cihazları tərəfindən dəstəklənir. Bu cür fayllardan GPS məlumatları geo-məkan məqsədləri üçün xəritəçəkmə proqramlarında göstərilmək üçün yüklənə bilər.

## GPX Fayl Formatı ##

GPX faylı enlik və uzunluq yeri məlumatlarından, yüksəklik dəyərlərindən və digər mümkün təsviri məlumatlardan ibarətdir. Yer məlumatları onluq dərəcələrlə, yüksəklik isə metrlə ifadə edilir. GPX faylındakı vaxt ISO 8601 formatından istifadə edərək Koordinasiya edilmiş Universal Saatdadır (UTC). GPX faylından istifadənin üstünlükləri aşağıdakılardır:

* GPX sizə Windows, MacOS, Linux, Palm və PocketPC üçün artan proqramlar siyahısı ilə məlumat mübadiləsi aparmağa imkan verir.

* GPX sadə veb səhifə və ya çevirici proqramdan istifadə edərək digər fayl formatlarına çevrilə bilər.

* GPX XML standartına əsaslanır, ona görə də istifadə etdiyiniz bir çox yeni proqramlar (məsələn, Microsoft Excel) GPX fayllarını oxuya bilər.

* GPX internetdəki hər kəs üçün sevimli proqramlarınızla dərhal işləyəcək yeni funksiyalar inkişaf etdirməyi asanlaşdırır.


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) istinad üçün GPX fayl formatının təqdimatını göstərir.

### Əsas Məlumat ###

Aşağıda GPS məlumatlarının təqdim edilməsi üçün GPX faylının bir hissəsi olan əsas məlumatlar verilmişdir.

* **Yol nöqtələri**: Yol nöqtəsi nöqtənin WGS84 (GPS) koordinatlarıdır və OGR tipli wkbPoint xüsusiyyətləri təbəqəsini təmsil edir

* **Marşrutlar**: OGR tipli wkbLineString xüsusiyyətləri təbəqəsini təmsil edir. Buraya təyinata aparan dönüş və ya mərhələ nöqtələrini göstərən keçid nöqtələri olan yol nöqtələrinin siyahısı daxildir

* **Tracks**: Tracks OGR tipli wkbMultiLineString xüsusiyyətləri qatını təmsil edir. O, yolu təsvir edən nöqtələrin ardıcıl siyahısında ara nöqtələri ehtiva edən ən azı bir seqmentdən ibarətdir. O, fasiləsiz GPS yolunu təmsil edən yol nöqtələrinin siyahısından ibarətdir.


### GPX Nümunə Faylı ###

Aşağıdakı GPX faylı GPX faylında GPS məlumatlarının təşkilini göstərir və GPX faylının məzmunu haqqında yaxşı fikir verə bilər.

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

## İstinadlar ##

* [GPX Fayl Formatı](https://www.topografix.com/gpx.asp)

* [GPX - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


