{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp MPK - Định dạng tệp gói bản đồ ArcGIS",
  "description":"Tìm hiểu về định dạng tệp MPK và các API có thể tạo và mở tệp MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-vi",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Tập tin MPK là gì?

Tệp MPK là tệp gói Bản đồ ArcGIS được tạo bằng ArcGIS. Nó chứa tài liệu bản đồ .mxd và dữ liệu liên quan. Ngoài ra, nó còn chứa thông tin bổ sung như các lớp được tham chiếu, ký hiệu và các tài nguyên khác. Tệp MPK được sử dụng để chia sẻ bản đồ và dữ liệu với những người dùng khác. Điều này giúp loại bỏ sự sẵn có của những người khác có nguồn dữ liệu gốc và cũng giúp phân phối bản đồ được sử dụng trên thiết bị di động.

## Định dạng tệp MPX

Chi tiết định dạng tệp nội bộ của tệp MPX không được cung cấp công khai để nhà phát triển tham khảo.

### Tạo tệp MPK bằng ArcGIS

Các tệp MPK có thể được tạo bằng ArcGIS. Tùy chọn Chia sẻ dưới dạng trong menu Gói bản đồ có thể được sử dụng để tạo tệp .mpk chứa tài liệu bản đồ cũng như tất cả dữ liệu và tài nguyên được tham chiếu của nó. Sau đó, tệp MPK này có thể được chia sẻ với người khác và có thể được mở trong ArcMap và ArcGIS Pro để xem bản đồ và dữ liệu.

### Tạo file MPK bằng Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Sử dụng Python để tạo gói bản đồ cho tất cả tài liệu bản đồ trong một thư mục

Mã Python sau đây tìm và tạo các gói bản đồ cho tất cả tài liệu bản đồ nằm trong một thư mục được chỉ định.

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

## Người giới thiệu

* [Bản đồ gói](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


