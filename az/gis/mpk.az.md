{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK Faylı - ArcGIS Xəritə Paketi Fayl Formatı",
  "description":"MPK fayl formatı və MPK faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-az",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## MPK faylı nədir?

MPK faylı ArcGIS ilə yaradılmış ArcGIS Xəritə paketi faylıdır. O, .mxd xəritə sənədini və əlaqəli məlumatları ehtiva edir. Bundan əlavə, o, istinad edilmiş təbəqələr, simvollar və digər resurslar kimi əlavə məlumatları ehtiva edir. MPK faylı xəritələri və məlumatları digər istifadəçilərlə bölüşmək üçün istifadə olunur. Bu, orijinal məlumat mənbəyinə malik başqalarının mövcudluğunu aradan qaldırır və həmçinin mobil cihazda istifadə olunacaq xəritələri yaymağa kömək edir.

## MPX fayl formatı

MPX fayllarının daxili fayl formatı təfərrüatları tərtibatçının arayışı üçün ictimaiyyətə açıq deyil.

### ArcGIS istifadə edərək MPK faylı yaradın

MPK faylları ArcGIS istifadə edərək yaradıla bilər. Xəritə Paketi menyusundakı Fərqlə Paylaş seçimi xəritə sənədini və onun bütün istinad edilmiş məlumat və resurslarını ehtiva edən .mpk faylı yaratmaq üçün istifadə edilə bilər. Bu MPK faylı daha sonra başqaları ilə paylaşıla bilər və xəritəyə və məlumatlara baxmaq üçün ArcMap və ArcGIS Pro-da açıla bilər.

### Python istifadə edərək MPK faylı yaradın

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Qovluqdakı bütün Xəritə Sənədləri üçün Xəritə Paketləri Yaratmaq üçün Python-dan istifadə edin

Aşağıdakı Python kodu müəyyən bir qovluqda yerləşən bütün xəritə sənədləri üçün xəritə paketlərini tapır və yaradır.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## İstinadlar

* [Paket Xəritəsi](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


