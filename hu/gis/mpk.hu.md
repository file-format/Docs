{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK fájl - ArcGIS térképcsomag fájlformátum",
  "description":"Ismerje meg az MPK fájlformátumot és az API-kat, amelyek MPK fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-hu",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Mi az MPK fájl?

Az MPK fájl egy ArcGIS Map csomagfájl, amelyet az ArcGIS segítségével hoztak létre. Egy .mxd térképdokumentumot és kapcsolódó adatokat tartalmaz. Ezenkívül további információkat is tartalmaz, például hivatkozott rétegeket, szimbólumokat és egyéb erőforrásokat. Az MPK fájl térképek és adatok megosztására szolgál más felhasználókkal. Ez kiküszöböli az eredeti adatforrással rendelkező többiek elérhetőségét, és elősegíti a mobileszközön használható térképek terjesztését is.

## MPX fájl formátum

Az MPX-fájlok belső fájlformátumának részletei nem állnak rendelkezésre nyilvánosan a fejlesztők számára.

### Hozzon létre MPK fájlt az ArcGIS segítségével

MPK fájlok az ArcGIS segítségével hozhatók létre. A Térképcsomag menü Megosztása másként opciójával létrehozhat egy .mpk fájlt, amely tartalmazza a térképdokumentumot és az összes hivatkozott adatot és erőforrást. Ez az MPK fájl ezután megosztható másokkal, és megnyitható az ArcMap és ArcGIS Pro alkalmazásban a térkép és az adatok megtekintéséhez.

### Hozzon létre MPK fájlt Python segítségével

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### A Python használatával térképcsomagokat hozhat létre egy mappában lévő összes térképdokumentumhoz

A következő Python-kód megkeresi és térképcsomagokat hoz létre az összes olyan térképdokumentumhoz, amely egy megadott mappában található.

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

## Hivatkozások

* [Csomagtérkép](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


