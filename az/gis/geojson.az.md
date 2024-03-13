{
  "date": "2019-10-11",
  "keywords": [
"geojson faylı",
"geojson faylı nədir",
"fayl",
"geojson nümunəsi",
"geojson fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON - JSON əsaslı Coğrafi Fayl Format",
  "description": "GeoJSON fayl formatı və GeoJSON fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-azn"
}
},
  "lastmod": "2019-09-10"
}

## GeoJSON faylı nədir?

GeoJSON, coğrafi xüsusiyyətləri öz qeyri-məkan atributları ilə təmsil etmək üçün nəzərdə tutulmuş JSON əsaslı formatdır. Bu format müxtəlif JSON (JavaScript Object Notation) obyektlərini və onların birləşmə modasını müəyyən edir. JSON formatı Coğrafi xüsusiyyətlər, onların məkan genişliyi və xassələri haqqında ümumi məlumatı təmsil edir. Bu faylın obyekti həndəsəni (Nöqtə, LineString, Poliqon), xüsusiyyəti və ya funksiyalar toplusunu göstərə bilər. Xüsusiyyətlər ünvanları və yerləri nöqtənin küçələri, əsas yollar və sərhədləri xətt sətirləri kimi, ölkələr, əyalətlər və quru bölgələri isə poliqon kimi əks etdirir. GeoJSON-dan istifadə edərək, müxtəlif mobil marşrutlaşdırma və naviqasiya proqramları öz xidmətlərinin əhatə dairəsini göstərə bilər. GeoJSON-un genişləndirilməsi ölçüsü daha kiçik olan və geoməkan topologiyasını kodlayan TopoJSON-dur.

## Qısa tarix ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON Fayl Format ##

### Koordinat ###

Koordinat istənilən coğrafi məlumatın əsas elementidir. Bu, tək ədədi (ondalıq format) təmsil edən tək ölçüdür (Uzunluq, Enlem) və bəzən yüksəklik üçün də koordinat yazır. Zaman da bir ölçüdür, lakin onun mürəkkəbliyi onu koordinat kimi qeyd etməyi çətinləşdirir. Hər iki JSON GeoJSON-da koordinatlar rəqəmlər kimi formatlanır.

### Vəzifə ###

Sıralanmış koordinat massivi [position](https://geojson.org/geojson-spec.html#positions)-ni təmsil edir. Bu, yer üzündə bir nöqtəni göstərə bilən ən kiçik vahiddir.

`[Uzunluq, enlik, yüksəklik]`

Cari spesifikasiyanın buraxılmasından əvvəl GeoJSON hər mövqe üçün üç koordinat qeyd etməyə icazə verdi, lakin yeni spesifikasiya ilə icazə verilmir.

### Həndəsə ###

Həndəsələr GeoJSON-da bir növdən və koordinatlar toplusundan ibarət sadə formalardır (nöqtələr, əyrilər və səthlər). Nöqtə tək bir mövqeyi təmsil edən ən sadə həndəsədir

`{ növ: Nöqtə, koordinatlar: [0, 0] }`

### LineStrings ###

Bir xətti təmsil etmək üçün ən azı iki əlaqəli yerdən istifadə olunur.

`{ tip: LineString, koordinatlar: [[10, 30], [10, 10]] }`

Nöqtə və xətt sətirləri həndəsənin ən sadə iki kateqoriyasıdır. Hər iki həndəsə növü bir çox həndəsi qaydaları narahat etmir. Nöqtə istənilən yerdə təmsil oluna bilər və nöqtələr öz-özünə kəsişsə belə, xətt birdən çox nöqtəyə malik ola bilər.

### Çoxbucaqlılar ###

GeoJSON həndəsələri Poliqonlarda əhəmiyyətli dərəcədə daha mürəkkəb görünür. Çoxbucaqlıların daxili və xarici sahələri var və içərisində dəliklər ola bilər.

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

LineStrings ilə müqayisədə, çoxbucaqlılarda, koordinat siyahısı daha bir səviyyəyə yerləşdirilib və dönər kimi kəsiklərə malik ola bilər.

### Koordinat Səviyyəsi ###

GeoJSON formatında koordinat xassəsi üçün dörd dərinlik səviyyəsi var.

### Xüsusiyyətləri ###

Həndəsələr GeoJSON-un mərkəzi hissəsidir, buna görə də real dünya məlumatları şəxsiyyət və atributlara malik olan sadə formalardan daha çoxdur. Xüsusiyyətlər həndəsəni və xassələrini qeyd edir.

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

Xüsusiyyət xassələri tək dərinlikli açar dəyər xəritələrini ehtiva edən [JSON](http://json.org/) obyekt növü ola bilər.

### Xüsusiyyətlər Kolleksiyası ###

GeoJSON fayllarının ən yüksək səviyyəsində FeatureCollection ən çox görülən şeydir:

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

Bir çox xəritəçəkmə və GIS proqram paketləri GeoDjango, OpenLayers və Geoforge proqramları da daxil olmaqla GeoJSON-u dəstəkləyir. O, həmçinin PostGIS və Mapnik ilə uyğun gəlir. Google, yahoo və Bing xəritələrinin API xidmətləri də GeoJSON-u dəstəkləyir.

## İstinadlar ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/GeoJSON)


