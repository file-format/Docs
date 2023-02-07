{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPK ファイル - ArcGIS マップ パッケージ ファイル形式",
  "description":"MPK ファイル形式と,MPK ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## .MPK オプション番号

MPK ファイルは、ArcGIS で作成される ArcGIS Map パッケージ ファイルです。 .mxd マップ ドキュメントと関連データが含まれています。さらに、参照レイヤー、シンボル、その他のリソースなどの追加情報が含まれています。 MPK ファイルは、マップとデータを他のユーザーと共有するために使用されます。これにより、元のデータ ソースを持つ他のユーザーを利用できなくなり、モバイル デバイスで使用するマップを配布するのにも役立ちます。

## MPX ファイル形式

MPX ファイルの内部ファイル形式の詳細は、開発者の参照用に公開されていません。

### ArcGIS を使用して MPK ファイルを作成する

MPK ファイルは、ArcGIS を使用して作成できます。 [マップ パッケージ] メニューの [共有] オプションを使用して、マップ ドキュメントとそのすべての参照データおよびリソースを含む .mpk ファイルを作成できます。その後、この MPK ファイルを他のユーザーと共有したり、ArcMap や ArcGIS Pro で開いてマップやデータを表示したりできます。

### Python を使用して MPK ファイルを作成する

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python を使用してフォルダー内のすべてのマップ ドキュメントのマップ パッケージを作成する

次の Python コードは、指定されたフォルダーにあるすべてのマップ ドキュメントのマップ パッケージを検索して作成します。

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

## 参考文献

* [パッケージ マップ](https://desktop.arcgis.com/ja/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

