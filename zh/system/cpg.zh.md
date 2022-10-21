{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG 文件格式 - ESRI 代码页文件",
  "description":"了解 CPG 文件格式和可以创建和打开 CPG 文件的 API。",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## 什么是一 .cpg 文件？

CPG 文件是一个可选文件，需要 ESRI 形状文件，用于指定用于识别要使用的字符集的代码页。这些以纯文本文件格式存储，并包含有关用于创建 shapefile 的编码的信息。如果 CPG 文件不可用，则 shapefile 使用系统默认编码。 CPG 文件（如果存在）必须与 [SHP](/zh/gis/shp/) 文件具有相同的前缀，例如，roads.shp、roads.cpg。

CPG 文件可以使用 ESRI ArcGIS Pro 打开。

### CPG 文件格式 - 更多信息

在 ArcCatalog 或任何其他 ArcGIS 应用程序中查看 shapefile 时，您只能看到 shapefile。但实际上，shapefile 使用与主 shape 文件一起读取的其他关联文件。如果 CPG 文件与主 SHP 文件一起出现，它也是其中之一。

## 参考

* [Shapefile 文件扩展名
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

