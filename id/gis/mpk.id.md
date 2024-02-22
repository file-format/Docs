{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File MPK - Format File Paket Peta ArcGIS",
  "description":"Pelajari tentang format file MPK dan API yang dapat membuat dan membuka file MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-id",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Apa itu file MPK?

File MPK adalah file paket Peta ArcGIS yang dibuat dengan ArcGIS. Ini berisi dokumen peta .mxd dan data terkait. Selain itu, ini berisi informasi tambahan seperti lapisan yang direferensikan, simbol, dan sumber daya lainnya. File MPK digunakan untuk berbagi peta dan data dengan pengguna lain. Hal ini menghilangkan ketersediaan sumber data asli lainnya dan juga membantu mendistribusikan peta untuk digunakan pada perangkat seluler.

## Format Berkas MPX

Detail format file internal file MPX tidak tersedia untuk umum untuk referensi pengembang.

### Buat File MPK Menggunakan ArcGIS

File MPK dapat dibuat menggunakan ArcGIS. Opsi Bagikan Sebagai di menu Paket Peta dapat digunakan untuk membuat file .mpk yang berisi dokumen peta dan semua data serta sumber referensinya. File MPK ini kemudian dapat dibagikan kepada orang lain dan dapat dibuka di ArcMap dan ArcGIS Pro untuk melihat peta dan data.

### Buat File MPK menggunakan Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Menggunakan Python untuk Membuat Paket Peta untuk semua Dokumen Peta dalam sebuah folder

Kode Python berikut menemukan dan membuat paket peta untuk semua dokumen peta yang berada di folder tertentu.

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

## Referensi

* [Peta Paket](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


