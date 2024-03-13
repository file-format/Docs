{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADF - ESRI ArcInfo Binary Grid Format",
  "description":"ADF faylları yarada və aça bilən ADF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf-az",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## ADF faylı nədir?

.adf uzantılı fayl ArcGIS, ArcView və ArcInfo kimi ESRI proqram proqramları tərəfindən istifadə edilən rastr məlumat faylı formatıdır. Məkan məlumatları ESRI üçün doğma olan ikili şəbəkə kimi saxlanılır. Şəbəkə həm tam, həm də üzən nöqtə ola bilən xanaların sətir və sütunlarından ibarətdir. ADF faylındakı tam torlar diskret məlumatları, üzən nöqtəli torlar isə davamlı məlumatları təmsil edir. Digər məşhur ESRI fayl formatı Coğrafi İnformasiya Sistemləri (GIS) proqramları tərəfindən istifadə ediləcək vektor məlumatları şəklində Geoməkan məlumatını təmsil edən [SHP](/gis/shp/) faylıdır.

## ADF Fayl Format - Ətraflı Məlumat

ADF faylları ikili şəbəkədə diskdə ikili fayllar kimi saxlanılır. Tam torlar dəyər atribut cədvəlində (ƏDV) saxlanılan atributlara malikdir. Şəbəkədəki hər bir unikal dəyər ƏDV-də bir qeydə malikdir, burada qeyd unikal dəyəri saxlayır və şəbəkədəki xanaların sayı həmin dəyərlə təmsil olunur.

Üzən nöqtəli şəbəkələrdə ƏDV yoxdur.

### Şəbəkə Strukturu

ADF faylının içərisində torlar kirəmitli raster məlumat strukturundan istifadə etməklə həyata keçirilir. Bu rastr məlumat strukturunun içərisindəki əsas vahid hüceyrələrdən ibarət düzbucaqlı blokdur. Hər bir blok diskdə saxlanılır və kafel adlanan dəyişən uzunluqlu fayl strukturunda sıxılır. Hər blok bir dəyişən uzunluqlu qeyd kimi saxlanılır.

GRID rasterləri iş məkanında saxlanılır, burada iş sahəsi hər GRID üçün bir məlumat alt kataloqu və alt kataloqu ehtiva edir. Müvafiq şəbəkə üçün coğrafi yeri və atribut məlumatları verən bir neçə fayl var. Məlumat alt kataloqu iş yerində GRID və əhatə dairələri kimi digər verilənlər dəstləri haqqında müəyyən məlumatları saxlayan bir neçə fayldan ibarətdir.

## İstinadlar ##

* [ESRI Grid Format](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)



