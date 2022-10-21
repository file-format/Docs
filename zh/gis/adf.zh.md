{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo 二进制网格格式",
  "description":"了解 ADF 文件格式和可以创建和打开 ADF 文件的 API。",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## 什么是一 .adf 文件？

扩展名为 .adf 的文件是 ESRI 软件应用程序（例如 ArcGIS、ArcView 和 ArcInfo）使用的栅格数据文件格式。空间数据存储为 ESRI 原生的二进制网格。网格由单元格的行和列组成，可以是整数也可以是浮点数。 ADF 文件中的整数网格表示离散数据，浮点网格表示连续数据。另一种流行的 ESRI 文件格式是 [SHP](/zh/gis/shp/) 文件，它以地理信息系统 (GIS) 应用程序使用的矢量数据形式表示地理空间信息。

## ADF 文件格式 - 更多信息

ADF 文件以二进制文件的形式保存到磁盘中的二进制网格中。整数网格具有存储在值属性表 (VAT) 中的属性。网格中的每个唯一值在增值税中都有一个记录，该记录存储唯一值，并且网格中的单元格数由该值表示。

浮点网格没有增值税。

### 网格结构

在 ADF 文件中，网格是使用平铺栅格数据结构实现的。此栅格数据结构内的基本单元是矩形单元块。每个块都存储在磁盘上并压缩成一个可变长度的文件结构，称为块。每个块存储为一个可变长度记录。

GRID 栅格存储在工作空间中，其中工作空间包含一个 info 子目录和每个 GRID 的子目录。有几个文件包含相应网格的地理位置和属性数据。 Info 子目录包含几个文件，这些文件维护有关工作空间中 GRID 和其他数据集（例如覆盖率）的某些信息。

## 参考 ＃＃

* [ESRI 网格格式](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [常见问题：Arc/INFO 网格的文件结构是什么？](https://support.esri.com/en/technical-article/000008526)

