{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPK-Datei - ArcGIS-Kartenpaket-Dateiformat",
  "description":"Erfahren Sie mehr über das MPK-Dateiformat und APIs, die MPK-Dateien erstellen und öffnen können.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Was ist eine MPK-Datei?

Eine MPK-Datei ist eine ArcGIS Map-Paketdatei, die mit ArcGIS erstellt wird. Es enthält ein MXD-Kartendokument und zugehörige Daten. Darüber hinaus enthält es zusätzliche Informationen wie referenzierte Layer, Symbole und andere Ressourcen. Die MPK-Datei wird verwendet, um Karten und Daten mit anderen Benutzern zu teilen. Dies eliminiert die Verfügbarkeit anderer, die über die ursprüngliche Datenquelle verfügen, und hilft auch bei der Verteilung von Karten, die auf einem mobilen Gerät verwendet werden sollen.

## MPX-Dateiformat

Die internen Dateiformatdetails von MPX-Dateien sind nicht öffentlich als Referenz für Entwickler verfügbar.

### MPK-Datei mit ArcGIS erstellen

MPK-Dateien können mit ArcGIS erstellt werden. Die Option „Freigeben als“ im Menü „Kartenpaket“ kann verwendet werden, um eine .mpk-Datei zu erstellen, die das Kartendokument und alle darauf referenzierten Daten und Ressourcen enthält. Diese MPK-Datei kann dann für andere freigegeben und in ArcMap und ArcGIS Pro geöffnet werden, um die Karte und die Daten anzuzeigen.

### MPK-Datei mit Python erstellen

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Verwenden von Python zum Erstellen von Kartenpaketen für alle Kartendokumente in einem Ordner

Der folgende Python-Code sucht und erstellt Kartenpakete für alle Kartendokumente, die sich in einem angegebenen Ordner befinden.

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

## Verweise

* [Paketübersicht](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

