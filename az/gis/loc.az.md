{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"fayl",
"uzadılması",
"fayl formatı",
"GPS Yeri",
"Yol nöqtəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC - GPS Yer Fayl Format",
  "description": "LOC fayl formatı və LOC faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-azc"
}
},
  "lastmod": "2021-07-18"
}

## LOC faylı nədir?

.loc uzantısı olan fayl, yol nöqtələri kimi coğrafi məkanları ehtiva edən GPS məkan faylıdır. Yol nöqtəsi Coğrafi İnformasiya Sistemi (GIS) tətbiqləri tərəfindən istifadə olunan yerə istinad edən bir cüt Enlem-Uzunluq dəyərləridir. DeLorme Topo kimi GPS xəritəçəkmə proqramları bu LOC fayllarında olan məlumatları son istifadəçilər tərəfindən seçilə bilən təbəqələr kimi oxumaq və göstərmək üçün LOC fayllarından istifadə edir. Bundan əlavə, bunlar tətbiqlər arasında GPS məlumatlarının mübadiləsi üçün istifadə olunur. LOC faylları [TopoGrafix EasyGPS](https://www.easygps.com/) kimi faylların məzmununu müvafiq geolokasiyada xəritədə təsvir edilmiş təbəqələr və verilənlər kimi göstərən proqramlardan istifadə etməklə açıla bilər.

## LOC Fayl Format - Ətraflı Məlumat

LOC fayllarının [GPX](/gis/gpx/) faylları ilə oxşarlıqları var, lakin fərqli formatda saxlanılır. Bunlar [XML](/web/xml/) faylları kimi saxlanılır, burada yol nöqtələrinin məzmunu və əlaqəli məlumat strukturlaşdırılmış teqlərdə yer alır. XML müxtəlif proqramlar arasında məlumat mübadiləsi üçün ümumiləşdirilmiş bir dil olduğundan, bu, LOC məlumatlarının digər proqramlarla mübadiləsini asanlaşdırır.

## LOC fayl formatı - Nümunə

Aşağıda LOC faylından bir keçid nöqtəsinin başlığı və mətni verilmişdir. Göründüyü kimi, başlıq məlumatı məlumat üçün yer mənbəyini ehtiva edir. Yol nöqtəsi 'ID' və yol nöqtəsi ilə əlaqəli məzmun datası kimi məlumatları ehtiva edir. Nəhayət, keçid nöqtəsi enlik və uzunluq dəyərlərinin və bu xüsusi keçid nöqtəsi ilə əlaqəli mətnin toplusudur.

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

## İstinadlar

* [TopGraphic EasyGPS](https://www.easygps.com/)


