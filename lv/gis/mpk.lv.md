{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK fails — ArcGIS kartes pakotnes faila formāts",
  "description":"Uzziniet par MPK faila formātu un API, kas var izveidot un atvērt MPK failus.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Kas ir MPK fails?

MPK fails ir ArcGIS Map pakotnes fails, kas izveidots ar ArcGIS. Tajā ir .mxd kartes dokuments un saistītie dati. Turklāt tajā ir ietverta papildu informācija, piemēram, atsauces slāņi, simboli un citi resursi. MPK fails tiek izmantots, lai kopīgotu kartes un datus ar citiem lietotājiem. Tas novērš pieejamību citiem, kam ir sākotnējais datu avots, kā arī palīdz izplatīt kartes lietošanai mobilajā ierīcē.

## MPX faila formāts

MPX failu iekšējā faila formāta informācija nav publiski pieejama izstrādātāju uzziņai.

### Izveidojiet MPK failu, izmantojot ArcGIS

MPK failus var izveidot, izmantojot ArcGIS. Izvēlnes Kartes pakotne opciju Kopīgot kā var izmantot, lai izveidotu .mpk failu, kurā ir kartes dokuments un visi tā atsauces dati un resursi. Pēc tam šo MPK failu var koplietot ar citiem, un to var atvērt programmās ArcMap un ArcGIS Pro, lai skatītu karti un datus.

### Izveidojiet MPK failu, izmantojot Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python izmantošana, lai izveidotu karšu pakotnes visiem kartes dokumentiem mapē

Šis Python kods atrod un izveido karšu pakotnes visiem kartes dokumentiem, kas atrodas noteiktā mapē.

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

## Atsauces

* [Pakotnes karte](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


