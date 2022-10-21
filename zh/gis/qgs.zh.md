{
  "date" : "2019-10-11",
  "keywords" :["qgs 文件","qgs 文件格式","什么是 qgs 文件","文件","qgs 示例","qgs 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS 项目文件格式",
  "description":"了解 QGS 文件格式和可以创建和打开 QGS 文件的 API。",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .qgs 文件？

带有.qgs 扩展名的文件是使用[QGIS]（https://www.qgis.org/en/site/）创建的项目文件，它是一个开源的跨平台GIS 应用程序。项目的所有项目设置，例如图层属性和辅助数据。它是在将地图项目保存到光盘时创建的。它实际上是一个配置文件，其中保留了诸如指向 GIS 数据的指针、有关图层的样式信息和项目标题等信息。 QGS 文件可以使用可免费下载的 QGIS 软件打开。

## QGS 文件格式

QGS 文件采用 [XML](/zh/web/xml/) 格式，并将项目数据存储为 XML 标签。 QGS 文件包含以下信息：

* 项目名称
* 项目 CRS
* 层树
*捕捉设置
* 关系
* 地图画布范围
* 项目模型
* 传奇
* mapview 码头（2D 和 3D）
* 具有底层数据集（数据源）链接的图层和其他图层属性，包括范围、SRS、连接、样式、渲染器、混合模式、不透明度等。
* 项目属性

### QGS 顶级 XML 标签

{{< figure src="../qgstoplevel.png" title="" >}}

### 扩展顶级项目层标签

{{< figure src="../qgstoplevel.png" title="" >}}

## 参考

* [QGIS](https://www.qgis.org/en/site/)

