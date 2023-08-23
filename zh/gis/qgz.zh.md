{
  "date" : "2021-03-18",
  "keywords" :[ "qgz 文件", "qgz 文件格式", "什么是 qgz 文件", "文件", "qgz 示例", "qgz 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - 量子 GIS 压缩项目",
  "description":"了解 QGZ 文件格式，它只是一个压缩的 QGS 和可以创建和打开 QGZ 文件的 API。",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## 什么是一 .qgz 文件？

**QGZ** 文件格式是包含 [QGS](/gis/qgs/) 文件和 QGD 文件的压缩存档。而 QGD 文件是 qgis 项目的 sqlite 数据库，由项目的辅助数据组成。如果没有辅助数据，QGD 文件将保持为空。

## 关于 QGZ 文件格式的详细信息

QGZ 是作为 **QGIS 3 项目文件格式**的新变体引入的。此格式是 QGS xml 文件的压缩容器。如果用户选择 QGD 作为可选格式，在这种情况下容器有利于存储辅助存储数据库。

在经典模式下，辅助数据库与 xml 文件一起保存为扩展名为 .qgd 的文件。选择压缩容器时，.qgd文件包含在.qgz中，方便用户使用，没有任何问题，用户共享项目文件时不能删除或忘记复制！


## 参考

* [QGZ – QGIS 的新默认项目文件格式](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS 文件格式](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

