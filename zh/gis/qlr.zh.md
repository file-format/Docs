{
  "date" : "2019-10-11",
  "keywords" :["qlr 文件","qlr 文件格式","什么是 qlr 文件","文件","qlr 示例","qlr 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS 图层定义文件",
  "description":"了解 QLR 文件格式和可以创建和打开 QLR 文件的 API。",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## 什么是一 .qlr 文件？

带有 .qlr 的文件是一个图层定义文件，其中包含指向图层数据源的指针。这是对图层的 [QGIS](https://www.qgis.org/en/site/) 样式信息的补充。该文件引用了所有相关样式，用作获取样式信息的数据的单一来源。使用 QLR 文件，数据源的信息可以放在这个单个文件中，其他应用程序可以读取该文件以加载样式信息。 QLR 文件可以使用任何文本编辑器（例如 Notepad++）打开。

## QLR 文件格式

QLR，类似于 [QGS](/zh/gis/qgs/)，是一个 XML 文件，它以 XML 标记的形式包含指向图层数据源的指针。它类似于 ArcGIS .lyr 文件。 QML 文件的顶级标签如下图所示。

{{< figure src="../qlr.png" title="" >}}

## 参考

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

