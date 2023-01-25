{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPK 文件 - ArcGIS 地图包文件格式”，
  "description":"了解 MPK 文件格式和可以创建和打开 MPK 文件的 API。”,
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## 什么是 .mpk 文件？

MPK 文件是使用 ArcGIS 创建的 ArcGIS 地图包文件。它包含一个 .mxd 地图文档和相关数据。此外，它还包含其他信息，例如参考图层、符号和其他资源。 MPK 文件用于与其他用户共享地图和数据。这消除了具有原始数据源的其他人的可用性，并且还有助于分发要在移动设备上使用的地图。

## MPX 文件格式

MPX 文件的内部文件格式细节不公开供开发者参考。

### 使用 ArcGIS 创建 MPK 文件

可以使用 ArcGIS 创建 MPK 文件。 “地图包”菜单中的“共享为”选项可用于创建包含地图文档及其所有引用数据和资源的 .mpk 文件。然后可以与其他人共享此 MPK 文件，并可以在 ArcMap 和 ArcGIS Pro 中打开以查看地图和数据。

### 使用 Python 创建 MPK 文件

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### 使用 Python 为文件夹中的所有地图文档创建地图包

以下 Python 代码为驻留在指定文件夹中的所有地图文档查找并创建地图包。

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

## 参考

* [封装地图](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

