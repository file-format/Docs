{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :["QGD","QGIS项目的Sqlite数据库","扩展","格式","QGIS","辅助数据库","什么是QGD文件"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - QGIS 项目的 Sqlite 数据库",
  "description":"了解 QGD，它是 QGIS 项目的 sqlite 数据库以及可以创建和打开 QGD 文件的 API。",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## 什么是一 .qgd 文件？

扩展名为.QGD文件的文件实际上是**QGIS**项目的关联sqlite数据库，容纳了项目的辅助数据。如果项目没有辅助数据，QGD 文件将保持为空。

## 关于 QGD 文件格式的详细信息

在经典模式下，辅助数据库与 xml 文件一起保存为扩展名为 .qgd 的文件。 **辅助数据库**系统允许在系统中读取和写入数据作为替代方式。在创建作为压缩容器的 QGZ 时，.qgd 文件包含在 .qgz 中。

## 什么是辅助数据库？
辅助数据库实际上是一个备用数据库系统，它是作为目标数据库复制的响应而创建的。辅助数据库实际上是重复数据库的一种情况，即您要复制到的数据库。例如，如果您使用重复数据库设置备用数据库，则源数据库将是目标数据库，备用数据库将被称为辅助数据库。


## 参考

* [QGZ – QGIS 的新默认项目文件格式](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS 文件格式](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

