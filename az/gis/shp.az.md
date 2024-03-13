{
  "date": "2019-10-11",
  "keywords": [
"shp faylı",
"shp fayl formatı",
"shp faylı nədir",
"fayl",
"shp nümunəsi",
"shp fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP - ESRI Shapefile",
  "description": "SHP faylları yarada və aça bilən SHP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-azp"
}
},
  "lastmod": "2019-09-10"
}

## SHP faylı nədir?

SHP ESRI Shapefile-nin təqdimatı üçün istifadə edilən əsas fayl növlərindən biri üçün fayl uzantısıdır. O, Coğrafi İnformasiya Sistemləri (CİS) tətbiqləri tərəfindən istifadə olunacaq vektor məlumatları şəklində coğrafi məlumatı təmsil edir. ESRI və digər proqram məhsulları arasında qarşılıqlı əlaqəni asanlaşdırmaq üçün format açıq spesifikasiyalar kimi işlənib hazırlanmışdır.

## Məlumatların təmsil olunması

Qeyd edildiyi kimi, şekil faylı formatı vektor xüsusiyyətləri kimi verilənlər dəstinin coğrafi məlumatını təsvir edir. Bu vektor xüsusiyyətlərinə aşağıdakılar daxildir:

* xal

* xətlər

* çoxbucaqlılar


Bu xüsusiyyətlər kombinasiyada su quyuları, ölkə sərhədləri, məkan nöqtələri, çayların axını, göllər və s. Məsələn, Los-Anceles şəhərlərini ehtiva edən bir şəkil faylı məkan məlumatlarını mənalı təmsil edən atributlar kimi şəhər adı və temperatura malik ola bilər.

## Əlaqədar Fayllar

Bağımsız bir shp faylı proqram proqramları tərəfindən tərkibindəki məlumatların mənasını vermək üçün istifadə edilə bilməz. Belə bir faylda olan məlumatı başa düşmək üçün bir forma faylı aşağıdakı əlavə məcburi fayllardan istifadə edir.

* shx faylı - indeks faylı

* dbf faylı - əsas faylda formaların bütün atributlarını saxlayan dBASE faylı

* prj faylı - faylın layihə məlumatlarını saxlayır


Əsas fayl ilə eyni adı paylaşan digər isteğe bağlı fayllar da ola bilər.

## SHP Fayl Formatının Xüsusiyyətləri

Shapefaylın açıq spesifikasiyalar ESRI-dən [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) formasında onlayn olaraq mövcuddur və faylın ümumi strukturunu təfərrüatı ilə işləyib hazırlayır. Əsas .shp faylındakı məlumat başlıqlardan və qeydlərdən ibarətdir. Sabit uzunluqlu fayl başlığının ardınca dəyişən uzunluqlu qeydlər gəlir, burada hər bir qeyd sabit uzunluqlu qeyd başlığından və sonra dəyişən uzunluqlu qeyd məzmunundan ibarətdir.

### Əsas SHP Fayl Başlığı

Əsas Fayl Başlığı faylın əvvəlindən başlayır və uzunluğu 100 baytdır. Bu əsas fayl başlığının bayt mövqeyi, dəyəri, növü və bayt sırası ilə birlikdə təşkili aşağıdakı cədvəldə göstərildiyi kimidir.


|Baytlar|Sahə|Dəyər|Növ|Bayt sırası
---|---|---|---|---|
|0-3|Fayl Kodu|9994|Bütün|Böyük Endian
|4-23|İstifadə olunmamış|0|Tam|Böyük Endian
|24-27|Fayl uzunluğu|Fayl uzunluğu|Tam ədəd|Böyük Endian
|28-31|Versiya|1000|Tam|Kiçik Endian
|32-35|Forma Tipi|Forma Tipi|Tam|Kiçik Endian
|36-67|Minimum Məhdudiyyətli Düzbucaqlı|Xmin, Ymin, Xmax və Ymax|double|Little Endian
|68-83|Bounding Box|Zmin, Zmax|double|Little Endian
|84-99|Bounding Box|Mmin, Mmax|double|

Qeyd etmək lazımdır ki, fayl uzunluğunun dəyəri, başlığı təşkil edən əlli 16 bitlik sözü də əhatə edən 16 bitlik sözlərdə faylın ümumi uzunluğudur.

#### Forma növləri

Yuxarıdakı cədvəldə forma növləri sahəsinin dəyərləri aşağıdakı kimidir:


|Dəyər|Forma növü
---|---|
|0|Null Forma
|1|Nöqtə
|3|Poliline
|5|Çoxbucaqlı
|8|Çox nöqtəli
|11|PointZ
|13|PolyLineZ
|15|ÇoxbucaqlıZ
|18|MultiPointZ
|21|PointM
|23|PolyLineM
|25|ÇoxbucaqlıM
|28|MultiPointM
|31|MultiPatch

### Məlumat Qeydləri ###

Əsas fayl başlığından sonra dəyişən uzunluqlu qeydlər gəlir, burada hər bir qeyd sabit uzunluqlu qeyd başlığından və sonra dəyişən uzunluqlu qeyd məzmunundan ibarətdir.

#### Başlığı qeyd edin ####

Qeyd başlığı 8 bayt sabit uzunluqda qeydin nömrəsi və məzmun uzunluğu haqqında məlumatları ehtiva edir. Qeyd başlığının təşkili aşağıdakı kimidir:


|Baytlar|Sahə|Dəyər|Növ|Bayt sırası
---|---|---|---|---|
|0-3|Qeyd nömrəsi|Qeyd nömrəsi|Tam ədəd|Böyük
|4-7|Rekord Uzunluq|Rekord Uzunluq|Bütün|Böyük

#### Məzmunu qeyd edin ####

Forma faylı qeydinin məzmunu forma növündən və sonra həmin forma üçün həndəsi məlumatdan ibarətdir. 0-lıq forma növü forma üçün həndəsi məlumatı olmayan boş formanı təmsil edir. Qeyd məzmununun uzunluğu forma hissələrinin və təpələrinin əksidir. Qeydin belə bir forma növü haqqında məlumatı necə ehtiva etdiyini öyrənmək üçün Nöqtə Şəkli növünə bir nümunə götürək.

Nöqtə X,Y qaydasında müəyyən coğrafi yeri təmsil edir, burada hər bir koordinat ikiqat dəqiqlikli dəyərlə təmsil olunur. Aşağıdakı cədvəl Nöqtə formasının növünü göstərir.


|Baytlar|Forma Tipi|Dəyər|Növ|Nömrə|Bayt Sırası
---|---|---|---|---|---|
|0-3|Forma Tipi|1|Tam|1|Kiçik
|4-11|X|X|ikiqat|1|Kiçik
|12-19|Y|Y|ikiqat|1|Kiçik

Examples of other shape types can be found the ESRI technical description document.

## İstinadlar ##

* [ESRI Shapefile Texniki Təsviri](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) ESRI tərəfindən


