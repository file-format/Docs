{
  "date": "2019-10-11",
  "keywords": [
"kmz faylı",
"kmz faylı nədir",
"fayl",
"kmz nümunəsi",
"kmz fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ - KML sıxılmış fayl formatı",
  "description": "KMZ faylları yarada və aça bilən KMZ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-azz"
}
},
  "lastmod": "2019-09-10"
}

## KMZ faylı nədir?

KMZ (KML Zipped) faylı Google Earth kimi GIS proqramlarında görünə bilən coğrafi məlumatı ehtiva edən sıxılmış [KML](/gis/kml/) faylının təsviridir. Yer nişanları haqqında məlumat faylda fərdi adla birlikdə enlik və uzunluq kimi təmsil olunur. Tək paketlənmiş KMZ faylı digər istifadəçilərlə asanlıqla paylaşıla bilər. KMZ faylları modelin geo-təmsil edilməsi üçün 3D model məlumatlarını da daxil edə bilər. KMZ faylı faylı onlayn məkanda saxlamaq və sonra URL-ni Google Xəritə Axtarış qutusuna yazmaqla Google Xəritədə aça bilər.

## Fayl strukturu ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Tətbiqlər kimi Google Earth-dən məlumatları birbaşa KMZ fayl formatına ixrac edə bilərsiniz. Əsas KML faylı **doc.kml** adlanır. KMZ faylını qablaşdırarkən ona birdən çox KML faylı əlavə etmək olar, lakin bunun heç bir faydası olmayacaq, çünki Google Earth KMZ faylını açarkən ilk KML faylını axtarır və onu oxuyur. Arxivdə tapılan hər hansı digər KML fayllarına məhəl qoymur. İstədiyiniz KML faylının Google Earth tərəfindən oxunduğundan əmin olmaq üçün KMZ faylının içərisinə yalnız bir KML faylının yerləşdirilməsi tövsiyə olunur.

doc.kml faylında istinad edilən şəkillər, modellər, teksturalar, səs faylları və digər resurslar əsas qovluğun daxilində başqa alt qovluğa yerləşdirilir. Bu, dəstəkləyici faylların sayından asılı olaraq bəzi mürəkkəbliyi də əhatə edə bilər. Bu tərkib mənbələrinə keçidlər nisbi və ya mütləq istinad vasitəsilə istinad edilə bilər.

### Nisbi İstinad ###

Resurslar əsas qovluq daxilində alt qovluqda əsas doc.kml ilə yanaşı yerləşdirildikdə, nisbi istinad aşağıdakı nümunədə göstərildiyi kimi bu dəstəkləyici fayllara işarə edə bilər (yalnız ikon üçün).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Mütləq İstinad ###

Resurslara tamamilə istinad edilə bilər. Mütləq istinadlar əlaqəli fayl üçün tam URL-i ehtiva edir. Fayllar mərkəzi serverdə yerləşdirildikdə, mütləq istinad onların nisbi istinadla müqayisədə birmənalı qalmasını təmin edir. Yerli fayla tamamilə istinad etmək tövsiyə edilmir, çünki fayllar yeni sistemə köçürüldükdə bu keçidlər pozulacaq. Mütləq istinad nümunəsi aşağıdakı kimidir:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Həmçinin bax ##

* [GeoJSON](/gis/geojson/)


## İstinadlar ##

* [Google Earth və KMZ Faylları](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


