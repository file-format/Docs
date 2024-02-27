{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK-fil - ArcGIS Map Package File Format",
  "description":"Lær om MPK-filformat og API'er, der kan oprette og åbne MPK-filer.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-da",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Hvad er en MPK fil?

En MPK-fil er en ArcGIS Map-pakkefil, der er oprettet med ArcGIS. Det indeholder et .mxd-kortdokument og relaterede data. Derudover indeholder den yderligere information såsom referencelag, symboler og andre ressourcer. MPK-fil bruges til at dele kort og data med andre brugere. Dette eliminerer tilgængeligheden af andre med den originale datakilde og hjælper også med at distribuere kort, der skal bruges på en mobilenhed.

## MPX filformat

De interne filformatdetaljer for MPX-filer er ikke offentligt tilgængelige til udviklerens reference.

### Opret MPK-fil ved hjælp af ArcGIS

MPK-filer kan oprettes ved hjælp af ArcGIS. Indstillingen Del som i menuen Kortpakke kan bruges til at oprette en .mpk-fil, som indeholder kortdokumentet og alle dets refererede data og ressourcer. Denne MPK-fil kan derefter deles med andre og kan åbnes i ArcMap og ArcGIS Pro for at se kortet og dataene.

### Opret MPK-fil ved hjælp af Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Brug af Python til at oprette kortpakker til alle kortdokumenter i en mappe

Den følgende Python-kode finder og opretter kortpakker til alle kortdokumenter, der ligger i en specificeret mappe.

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

## Referencer

* [Pakkekort](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


