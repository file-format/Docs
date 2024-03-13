{
  "date": "2021-07-29",
  "keywords": [
"gpkg faylı",
"gpkg fayl formatı",
"gpkg faylı nədir",
"fayl",
"gpkg nümunəsi",
"gpkg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG - GeoPackage Format Faylları",
  "description": "GPKG fayl formatı və GPKG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## GPKG faylı nədir?
.gpkg genişləndirilməsi olan fayl, tipik təriflər, format məhdudiyyətləri, bütövlüyü təsdiqləmələri və məzmun məhdudiyyətləri olan verilənlər və metadata cədvəllərindən ibarət SQLite verilənlər bazası konteyneri kimi həyata keçirilən coğrafi məlumat sistemindən ibarətdir. 2014-cü ildə nəşr edilmişdir; ABŞ ordusu adından OGC (Açıq Geoməkan Konsorsiumu) tərəfindən müəyyən edilmişdir. Müxtəlif hökumətlər, kommersiya və açıq mənbə təşkilatları GeoPackage-i geniş şəkildə dəstəkləyir.

## GPKG fayl formatı
GeoPackage genişləndirilmiş SQLite 3 verilənlər bazası faylı kimi hazırlanır; standart aşağıdakılar üçün bir sıra qaydalar (tələb olunan konvensiyalar) müəyyən edir:
- Görüntülərin kafel matris dəstlərinin saxlanması
- Vektor xüsusiyyətləri
- Müxtəlif miqyasda rastr xəritələri
- Metadata və sxem

Siz standartın 2.3-cü bəndində müəyyən edilmiş genişləndirmə qaydalarından istifadə etməklə GeoPackage-ni genişləndirə bilərsiniz. GeoPackage dizaynının məqsədi mümkün qədər yüngül verilənlər bazası yaratmaq və onu istifadəyə hazır tək fayla daxil etmək idi. Bu, onu oflayn rejimdə mobil proqramlar və bulud yaddaşında və ya USB yaddaş cihazlarında sürətli paylaşma üçün ideal hala gətirir.

### GPKG məzmunu
GeoPackages digər əlaqəli verilənlər bazaları kimi bir sıra cədvəllərdən ibarətdir. Bu cədvəllər istifadəçi tərəfindən müəyyən edilmiş və ya metadata cədvəlləri ola bilər. GeoPackages iki məcburi metadata cədvəlindən ibarətdir:

#### gpkg_məzmunu
GeoPackage üçün məzmun cədvəli. Bu cədvəldəki məcburi sütunlar:

- **cədvəlin_adı**: istifadəçi tərəfindən müəyyən edilmiş verilənlər cədvəlinin faktiki adı;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x və max_y**: məzmunun məkan genişlikləri. ;
- **srs_id**: məkan istinad sistemi.

#### gpkg_spatial_ref_sys
Məkan istinad məzmunu üçün; plitələr və xüsusiyyətlər daxil olmaqla, lakin bunlarla məhdudlaşmayaraq, məzmundakı hər bir sıra koordinat istinad sisteminə istinad etməlidir; **gpkg_spatial_ref_sys** cədvəlində saxlanılır. Bu cədvəldəki məcburi sütunlar:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-aze;
- **təşkilat**: Müəyyən edən təşkilatın hərflərə həssas olmayan adı.
- **organization_coordsys_id**: Təşkilat tərəfindən təyin edilmiş SRS-in rəqəmli ID-si;
- **tərif**: SRS-in tanınmış mətn tərifi.


## İstinadlar

* [GeoPackage - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/GeoPackage)

* [GeoPackage ilə Başlarkən](http://www.geopackage.org/guidance/getting-started.html)


