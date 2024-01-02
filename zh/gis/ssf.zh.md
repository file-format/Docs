{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - Trimble 标准存储格式文件",
  "description":"了解 SSF 文件格式和可以创建和打开 SSF 文件的 API。",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是一 .ssf 文件？

带有 .ssf 文件的文件是 [Trimble](https://www.trimble.com) 导航 GIS 软件应用程序使用的地理空间数据存储文件格式。它存储使用 Trimble 设备从现场记录的 GPS 数据。然后将 GPS 日志导入 Trimble 应用程序套件的其中一个应用程序中。 SSF 中包含的 GPS 日志用于创建自定义坐标系。 SSF 文件可以使用 [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/en/products/software/office-software)、Trimble Navigation GPS Pathfinder Tools SDK 和 ESRI ArcGIS for Desktop 打开Trimble GPS Analyst 插件。

## SSF 文件格式 - 更多信息

当 GPS 数据从 Trimble 设备传输到计算机进行后处理时，所有这些文件都被合并到一个 .ssf 文件中。后处理软件使用此原始未处理文件进行更正并帮助数据管理。

SSF 文件以 Trimble 专有文件格式存储到光盘中，其详细规格不公开。它特定于 Trimble 设备并代表 GPS 单元的数据。迄今为止，没有非商业免费的解决方案可用于读取或转换 SSF 文件。

## 参考

* [Trimble 新闻稿](https://www.trimble.com/news/release.aspx?id=050510b)

