{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK-fil - ArcGIS Map Package File Format",
  "description":"Lär dig om MPK-filformat och API:er som kan skapa och öppna MPK-filer.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-sv",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Vad är en MPK fil?

En MPK-fil är en ArcGIS Map-paketfil som skapas med ArcGIS. Den innehåller ett .mxd-kartdokument och relaterade data. Dessutom innehåller den ytterligare information som refererade lager, symboler och andra resurser. MPK-filen används för att dela kartor och data med andra användare. Detta eliminerar tillgängligheten för andra som har den ursprungliga datakällan och hjälper också till att distribuera kartor som ska användas på en mobil enhet.

## MPX filformat

De interna filformatsdetaljerna för MPX-filer är inte tillgängliga offentligt för utvecklarens referens.

### Skapa MPK-fil med ArcGIS

MPK-filer kan skapas med ArcGIS. Alternativet Dela som i menyn Map Package kan användas för att skapa en .mpk-fil som innehåller kartdokumentet och alla dess refererade data och resurser. Denna MPK-fil kan sedan delas med andra och kan öppnas i ArcMap och ArcGIS Pro för att se kartan och data.

### Skapa MPK-fil med Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Använda Python för att skapa kartpaket för alla kartdokument i en mapp

Följande Python-kod hittar och skapar kartpaket för alla kartdokument som finns i en angiven mapp.

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

## Referenser

* [Paketkarta](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


