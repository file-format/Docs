{
  "date" : "2019-10-11",
  "keywords" :["qml 文件","qml 文件格式","什么是 qml 文件","文件","qml 示例","qml 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - QGIS 样式文件格式",
  "description":"了解 QML 文件格式和可以创建和打开 QML 文件的 API。",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## 什么是一 .qml 文件？

带有 .qml 扩展的文件是一个 XML 文件，用于存储 QGIS 图层的图层样式信息。 QGIS 是一个开源的跨平台 GIS 应用程序，用于显示地理空间数据，具有以图层形式组织数据的能力。 QML 文件包含 QGIS 用于呈现特征几何图形的信息，包括符号定义、大小和旋转、标签、不透明度、混合模式等等。与 QLR 文件不同，QML 文件本身包含所有样式信息。 QML 文件可以在任何文本编辑器中打开，例如 Notepad++。

## QML 文件格式

QLR 与 [QGS](/zh/gis/qgs/) 和 [QLR](/zh/gis/qlr/) 类似，是一个包含图层样式信息的 XML 文件。

下图显示了 QML 文件的顶级标签（仅 renderer_v2 及其符号标签展开）。

{{< figure src="../qml.png" title="" >}}

## 参考

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

