{
  "date": "2020-03-16",
  "keywords": [
"PAT faylı",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PAT fayl formatı və PAT faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "PAT fayl formatı",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-azt"
}
},
  "lastmod": "2020-10-25"
}

## PAT faylı nədir?

.pat uzantılı fayl AutoCAD proqramı tərəfindən istifadə edilən CAD faylıdır. PAT fayllarını aça bilən proqramlar bu fayllarda saxlanılan lyuk modelindən istifadə edir, sahənin teksturası/doldurulması haqqında məlumat alır. Tərkibindəki naxışlar çəkilmiş obyektlərə materialın görünüşü haqqında məlumat verir. PAT faylları Autodesk AutoCAD, CorelDRAW Graphics Suite və Ketron Software kimi proqramlarda açıla bilər. PAT faylları JPG, PNG, BMP və s. kimi müxtəlif şəkil formatlarına çevrilə bilər.

## PAT fayl formatı

PAT faylları düz mətn formatında yazılır və istənilən mətn redaktorunda aça bilər. Bu fayllardakı lyuk patterləri vektor əsaslıdır və AutoCAD sənədlərində göstərilən sintaksisə əməl edir.

Bütün nümunələr 0,0 nöqtəsindən başlayır, naxış lyukçuluq sərhədini əhatə etmək üçün hesablanır.

### Nümunə Tərifi

Bütün nümunə tərifləri aşağıdakı sahələrdən ibarətdir:
 * Aparıcı '\*
 * Ad - Adda boşluq, durğu işarələri, mötərizə və ya kəsik işarələri ola bilməz.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### Hatch Pattern Nümunələri
Aşağıda kvadrat naxış nümunəsi verilmişdir
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Paraleloqram nümunəsini göstərən başqa bir nümunə aşağıdakı kimidir.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## İstinadlar ##

 * [Autodesk tərəfindən Hash Nümunələri](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

