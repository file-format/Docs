{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SDF 文件 - 空间数据格式文件",
  "description":"了解 SDF 文件格式和可以创建和打开 SDF 文件的 API。”,
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## 什么是 .sdf 文件？

空间数据文件 (SDF) 是由 Autodesk 开发的地理数据库文件格式。它存储地理空间数据，并由 Autodesk GIS 程序 MapGuide 和 AutoCAD Map 3D 使用。 SDF 文件格式基于单文件数据库文件格式 SQLite3。它被认为是大型空间信息数据集的优化文件格式。

您可以使用 Autodesk AutoCAD Map 3D 2022 和 Autodesk AutoCAD Civil 3D 2023 打开 SDF 文件。

## SDF 文件格式 - 更多信息

SDF 文件格式作为二进制文件存储到光盘。它基于 SQLite 数据库，利用低级存储组件对数据进行二进制序列化。 SDF 文件包含每个文件的多个要素类和每个要素类的多个几何属性。由于使用 R 树对每个几何属性进行索引，因此可以高速访问 SDF 文件中的数据。

## 参考

* [SDF 数据格式](https://en.wikipedia.org/wiki/Spatial_Data_File)
* [导入 Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

