{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AUX - 辅助文件",
  "description":"了解 AUX 文件格式和可以创建和打开 AUX 文件的 API。",
  "linktitle" : "AUX_GIS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是一 .aux 文件？

带有 .aux 扩展名的文件是一个辅助文件，其中包含 [.JPG](/zh/image/jpeg/) 或 GeoTIFF [.TIFF](/zh/image/tiff/) 文件中伴随的栅格数据文件的地理空间数据。由于光栅文件不能保存此类信息，因此 AUX 文件用于以关联数据的形式存储附加信息。这些通常存储在与相应光栅文件名相同的文件名的同一目录中。 AUX 文件通常由 ESRI ArcGIS Desktop 和 ERDAS IMAGINE 等地理空间应用程序使用。

## AUX 文件格式 - 更多信息

AUX 文件包含相关信息，例如颜色图、坐标系信息、变换数据、投影信息和统计信息。这些信息可能并不总是与地理图像一起提供，并且可能由 GIS 程序生成。

## 参考

* [ERDAS IMAGINE - 支持的文件格式](https://www.hexagongeospatial.com/products/power-portfolio/erdas-imagine#imagine-technical-documents)

