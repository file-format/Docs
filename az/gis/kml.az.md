{
  "date": "2019-10-11",
  "keywords": [
"kml faylı",
"kml faylı nədir",
"fayl",
"kml nümunəsi",
"kml fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML - Keyhole Markup Language",
  "description": "KML faylları yarada və aça bilən KML fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-azl"
}
},
  "lastmod": "2019-09-10"
}

## KML faylı nədir?

KML, Keyhole Markup Language) XML notasiyasında coğrafi məlumatı ehtiva edir. KML kimi saxlanılan fayllar Coğrafi İnformasiya Sistemi (GIS) proqramlarında açıla bilər, o şərtlə ki, onlar onu dəstəkləsinlər. Bir çox proqramlar KML fayl formatı beynəlxalq standart kimi qəbul edildikdən sonra onu dəstəkləməyə başlamışdır. KML daxili elementləri və atributları olan etiket əsaslı strukturdan istifadə edir. Bütün teqlər böyük hərflərə həssasdır və [KML](https://developers.google.com/kml/documentation/kmlreference) İstinad əsasında bu teqlərin sırasına riayət etmək vacibdir.

## Qısa tarix ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Format Google Earth ilə istifadə üçün işlənib hazırlandığından o, KML fayllarına ilk baxan və redaktə edən kimi fərqlənir. Zaman keçdikcə, müxtəlif dillərdə bir neçə API daxil olmaqla, KML fayl formatlarına dəstək verən daha çox layihə var.

## KML Fayl Formatının Xüsusiyyətləri ##

KML Referansı tam fayl formatının spesifikasiyasına malik olmaq üçün istinad üçün tam bələdçidir. Standart KML faylı aşağıdakılardan ibarətdir:

* Yer nişanları

* Təsviri HTML-də yer nişanları

* Yer örtükləri

* Yollar

* Çoxbucaqlılar


Bunlara əlavə olaraq, KML faylının təkmil versiyasında aşağıdakılar ola bilər:

* Həndəsə üçün üslublar

* Vurğulanmış nişanlar üçün üslublar

* Ekran örtükləri

* Şəbəkə Bağlantıları


KML elementinin hər biri faylda mövcud olan məlumatı geo-yerləşdirən uzunluqlu məlumatlara malikdir. Bununla belə, başlıq, hündürlük və əyilmə kimi əlavə parametrlər ola bilər.

### Yer İşarələri ###

Yer səthində bir mövqeyi təmsil etmək üçün istifadə olunur və tərəfindən müəyyən edilir<Point> element. Aşağıda yer nişanının KML faylında necə təmsil olunduğuna dair bir nümunə verilmişdir.

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

### Yer İşarələrində təsviri HTML ###

Əlavə məlumat yer nişanının təsvirini daha da gücləndirən yer nişanı ilə əlaqələndirilə bilər. Bu cür məlumatlara keçidlər, şrift ölçüləri, üslublar və rənglər daxildir. Bundan əlavə, o, həmçinin yer nişanının bir hissəsi olmaq üçün mətn düzülməsini və cədvəlləri ehtiva edir.

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

### Torpaq örtükləri ###

Bunlar görüntünün Yer səthinə təbəqələşməsini təmsil edir. The<icon> element üst şəkil faylına keçidi ehtiva edir.

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

### Yollar ###

Yollar ilə təmsil olunur<LineString> uzunluqlu cütlərin toplusu olan element. Bunlardan istifadə etməklə Google Earth-də çoxlu müxtəlif növ yollar yaradıla bilər.

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

## KML faylında məkan istinadı ##

Coğrafi Məkanlar haqqında hər hansı bir Geoməkan faylında olan məlumat məkan istinad məlumatı olmadan fərqli mənalara malik ola bilər. Varsayılan olaraq, KML faylının məkan istinadı 1984-cü il Dünya Geodeziya Sistemi, WGS84 tərəfindən müəyyən edilir.

## İstinadlar ##

* [KML Reference](https://developers.google.com/kml/documentation/kmlreference)

* [KML üçün Google Tərtibatçı Təlimatı](https://developers.google.com/kml/documentation/kml_tut)

* [KML Fayl Format](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


