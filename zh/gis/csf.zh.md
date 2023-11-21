{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSF 文件 - GeoMedia 坐标系统文件格式",
  "description":"了解 CSF 文件格式以及可以创建和打开 CSF 文件的 API。",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## 什么是 .csf 文件？

CSF 文件是一个坐标系文件，其中包含有关 GIS 文件坐标系的信息。 Intergraph 的 GeoMedia 软件使用它来定义特定坐标系的参数。其中包括诸如基准、投影和测量单位等信息参数。此信息用于为没有坐标系的输出数据生成地图。 GeoMedia 使用此信息在正确的坐标系中正确显示和操作地理数据。

## CSF 文件格式

CSF 文件存储为文本文件，其中包含地理坐标系的详细信息。 GeoMedia 允许从未定义坐标系的输入数据导入地理信息文件。 GIS 系统使用投影和坐标系统显示具有精确值的地图文件。 CSF 文件在与输出文件相同的位置创建。

## 参考

* [如何正确地将 shapefile 数据显示或提供到 GeoMedia 中？
](https://supportsi.hexagon.com/help/s/article/How-do-you- Correctly-display-or-serve-shapefile-data-into?language=en_US)

