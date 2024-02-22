{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor MPK – formát souboru mapového balíčku ArcGIS",
  "description":"Přečtěte si o formátu souboru MPK a rozhraních API, která mohou vytvářet a otevírat soubory MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-cs",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Co je soubor MPK?

Soubor MPK je soubor balíčku ArcGIS Map, který je vytvořen pomocí ArcGIS. Obsahuje mapový dokument .mxd a související data. Kromě toho obsahuje další informace, jako jsou odkazované vrstvy, symboly a další zdroje. Soubor MPK se používá ke sdílení map a dat s ostatními uživateli. To eliminuje dostupnost ostatních, kteří mají původní zdroj dat, a také pomáhá distribuovat mapy pro použití na mobilním zařízení.

## Formát souboru MPX

Podrobnosti o interním formátu souborů MPX nejsou pro vývojáře veřejně dostupné.

### Vytvořte soubor MPK pomocí ArcGIS

Soubory MPK lze vytvářet pomocí ArcGIS. Volbu Sdílet jako v nabídce Mapový balíček lze použít k vytvoření souboru .mpk, který obsahuje mapový dokument a všechna jeho odkazovaná data a zdroje. Tento soubor MPK lze poté sdílet s ostatními a lze jej otevřít v aplikacích ArcMap a ArcGIS Pro a zobrazit mapu a data.

### Vytvořte soubor MPK pomocí Pythonu

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Použití Pythonu k vytvoření mapových balíčků pro všechny mapové dokumenty ve složce

Následující kód Pythonu vyhledá a vytvoří balíčky map pro všechny mapové dokumenty, které jsou umístěny v zadané složce.

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

## Reference

* [Mapa balíčku](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


