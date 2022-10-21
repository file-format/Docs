{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - ESRI 空间索引二进制文件",
  "description":"了解 SBN 文件格式和可以创建和打开 SBN 文件的 API。",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## 什么是一 .sbn 文件？

扩展名为 .sbn 的文件是与 ESRI ArcGIS [.shp](/zh/gis/shp/) 文件相关联的空间索引文件。它用于在对数据执行索引时优化空间查询。与 .sbn 一起使用的另一种文件类型是 .sbx 文件。 SBN 和 SBX 文件共同构成一个形状索引，以加快空间查询。 SBN 文件是可选的，可以使用 [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview) 打开。

## SBN 文件格式 - 更多信息

SBN 文件以二进制文件的形式存储到光盘中，并且它们的内部文件格式详细信息不可用。这些存储空间查询的 SHP 文件的二进制表示。 SBX 索引文件与 SBN 文件一起使用，以加快对 shapefile 的空间查询。

## 参考

* [ESRI ShapeFile 技术说明](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

