{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MPK File - ArcGIS Map Package File Format",
  "description":"Learn about MPK file format and APIs that can create and open MPK files.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
    }
  },
  "lastmod" : "2022-12-19"
}

## What is an MPK file?

An MPK file is an ArcGIS Map package file that is created with ArcGIS. It contains a .mxd map document and related data. In addition, it contains additional information such as referenced layers, symbols, and other resources. MPK file is used to share maps and data with other users. This eliminates the availability of others having the original data source and also helps to distribute maps to be used on a mobile device.

## MPX File Format

The internal file format details of MPX files are not available publicly for developer's reference.

### Create MPK File Using ArcGIS

MPK files can be created using ArcGIS. The "Share As" option in the "Map Package" menu can be used to create a .mpk file which contains the map document and all of its referenced data and resources. This MPK file can then be shared with others and can be opened in ArcMap and ArcGIS Pro to view the map and data.

### Create MPK File using Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Using Python to Create Map Packages for all Map Documents in a folder

The following Python code finds and creates map packages for all map documents that reside in a specified folder.

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

## References

* [Package Map](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)
