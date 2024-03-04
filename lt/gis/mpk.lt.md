{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK failas – ArcGIS žemėlapio paketo failo formatas",
  "description":"Sužinokite apie MPK failo formatą ir API, kurios gali kurti ir atidaryti MPK failus.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Kas yra MPK failas?

MPK failas yra ArcGIS žemėlapio paketo failas, sukurtas naudojant ArcGIS. Jame yra .mxd žemėlapio dokumentas ir susiję duomenys. Be to, jame yra papildomos informacijos, pvz., nurodytų sluoksnių, simbolių ir kitų išteklių. MPK failas naudojamas bendrinti žemėlapius ir duomenis su kitais vartotojais. Tai pašalina prieinamumą kitiems, turintiems pradinį duomenų šaltinį, taip pat padeda platinti žemėlapius, kurie bus naudojami mobiliajame įrenginyje.

## MPX failo formatas

Išsami MPX failų vidinio formato informacija nėra viešai prieinama kūrėjui.

### Sukurkite MPK failą naudodami ArcGIS

MPK failus galima sukurti naudojant ArcGIS. Meniu Žemėlapio paketas esančią parinktį Bendrinti kaip galima naudoti kuriant .mpk failą, kuriame yra žemėlapio dokumentas ir visi su juo susiję duomenys bei ištekliai. Šis MPK failas gali būti bendrinamas su kitais ir gali būti atidarytas ArcMap ir ArcGIS Pro, kad būtų galima peržiūrėti žemėlapį ir duomenis.

### Sukurkite MPK failą naudodami Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python naudojimas visų žemėlapių dokumentų aplanke žemėlapių paketams kurti

Šis Python kodas suranda ir sukuria žemėlapių paketus visiems žemėlapio dokumentams, kurie yra nurodytame aplanke.

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

## Nuorodos

* [Paketo žemėlapis](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


