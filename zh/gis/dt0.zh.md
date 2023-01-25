{
  "date" : "2022-12-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DT0 文件 - DTED 0 级文件格式",
  "description":"了解 DT0 文件格式和可以创建和打开 DT0 文件的 API。",
  "linktitle" : "DT0",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-07"
}

## 什么是 .dt0 文件？

DT0 文件是一种数字地形高程数据 (DTED) 文件，其中包含用于研究地形高程数据的 0 级信息。高程数据在 DT0 文件中均匀分布，可以通过流行的 GIS 程序读取，例如 ESRI ArcGIS Pro、TatukGIS、Blue Marble Geographic Global Mapper 和 Pitney Bowes MapInfo。 DT0 文件主要被科技界用来研究全球地形的坡度、高程和表面粗糙度。

DT0 文件格式类似于 [DT1](/zh/gis/dt1/) 和 [DT2](/zh/gis/dt2/) 文件类型，但粒度更小。

### DT0 文件格式

DT0 文件作为二进制文件保存到光盘。这些可以使用许多 GIS 应用程序读取。 DT0 文件可以合并到一个文件地理数据库栅格目录中，该目录可用于创建一个大马赛克。

## 如何将光栅转换为 DTED 文件？

有多种工具可以将光栅转换为 DTED 文件。 [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) 就是这样一种可以将栅格转换为 DTED 的工具.

## 参考

* [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
* [KML 文件格式](/zh/gis/kml/)

