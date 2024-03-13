{
  "date": "2021-07-30",
  "keywords": [
"dlg faylı",
"dlg fayl formatı",
"dlg faylı nədir",
"fayl",
"dlg nümunəsi",
"dlg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "DLG - Shapefile Shape Index Format",
  "description": "DLG faylları yarada və aça bilən DLG fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dl-azg"
}
},
  "lastmod": "2021-07-30"
}

## DLG faylı nədir?
.dlg uzantılı faylda ABŞ Geoloji Tədqiqat Xidməti (USGS) tərəfindən idarə olunan rəqəmsal vektor formasında göstərilən kartoqrafik xəritə xüsusiyyəti olan Rəqəmsal Xətt Qrafiki var. DLG faylları iki müxtəlif formatda mövcuddur:
1. **Könüllü format**: 80 baytlıq məntiqi qeyd uzunluğunu, UTM yer koordinat sistemini və xətt, qovşaq və sahə elementlərində olan topologiya əlaqələri özündə birləşdirən sadə istifadə formatı.
2. **Spatial Data Transfer Standard (SDTS) formatı**: müxtəlif kompüter sistemləri arasında məkan məlumatlarının ötürülməsini asanlaşdıran format.

## DLG fayl formatı
DLG fayl formatı USGS xəritələri üçün nəzərdə tutulmuşdur və doqquz fərqli xüsusiyyət kateqoriyası ilə böyük, orta və kiçik miqyasda ötürülür. DLG faylları xəritəçəkmə və GIS proqramlarında istifadə üçün topoloji strukturlaşdırılmış isteğe bağlı və Məkan Məlumatlarının Ötürmə Standartı (SDTS) formatlarında gəlir.
### DLG Fayl Formatının Xüsusiyyətləri
DLG faylları üç fərqli miqyasda paylanır:

1. **Böyük miqyaslı** - adətən uyğundur:
- USGS 7,5-7,5 dəqiqə
- 1:24,000 və 1:25,000 miqyaslı topoqrafik dördbucaqlı xəritə seriyası
- Alyaska üçün 1:63,360-miqyaslı
- Puerto Riko üçün 1:30,000-miqyaslı
 
2. **Aralıq miqyas** - USGS-dən əldə edilmişdir: 
- 30-60 dəqiqə
- 1:100,000 miqyaslı xəritə seriyası
3. **Kiçik miqyaslı** - ABŞ Milli Atlasının USGS 1:2,000,000 miqyaslı bölmə xəritələrindən əldə edilmişdir
### Məlumat Kateqoriyaları
Nine different categories of layers, or features, are available in DLG files:
1. İctimai Torpaq Tədqiqat Sistemi (PLSS)
2. Sərhədlər (BD)
3. Nəqliyyat (TR)
4. Hidroqrafiya (HY)
5. Hipsoqrafiya (HP)
6. Bitki mənşəli olmayan xüsusiyyətlər (NV)
7. Sorğuya nəzarət və markerlər (SM) 
8. Süni xüsusiyyətlər (MS) 
9. Bitki səthi örtüyü (SC)

Böyük miqyaslı DLG faylları doqquz təbəqənin hamısını təklif edir, orta miqyaslı isə PLSS, BD, TR, HY və HP-nin beş qatını təklif edir. Kiçik miqyaslı DLG-lər PLSS, BD, TR, HY və MS-in beş qatını təklif edir.

## İstinadlar

* [Rəqəmsal xətt qrafiki - Wikipedia tərəfindən)](https://en.wikipedia.org/wiki/Digital_line_graph)



