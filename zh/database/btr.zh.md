{
  "date" : "2021-09-06",
  "keywords" :["btr","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","Btrieve 数据库"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 BTR 文件格式和可以创建和打开 BTR 文件的 API。",
  "title" :"BTR - Btrieve 数据库文件",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## 什么是一 .btr 文件？

带有 .btr 扩展名的文件是由 [Btrieve](https://www.actian.com/) 事务数据库应用程序创建的数据库文件。与关系数据库管理系统 (RBMS) 不同，Btrieve 基于索引顺序访问方法 (ISAM)，这是一种存储数据以便快速检索的方法。 BTR 文件存储记录的集合，并用于根据要求生成报告。 BTR 文件可以使用 Pervasive Btrieve Database Manager、Pervasive PSQL Maintenance Utility 和 Legend Software BTRIEVE Viewer 打开。

## BTR 文件结构 - 更多信息

BTR 文件结构中每个字节的内部数据结构和对齐方式不公开。然而，Btrieve
提供 [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) 可用于从 BTR 文件中读取信息。它与以下编程语言和开发环境兼容。

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* 微焦点 COBOL
*微软Visual Basic
* 微软 Visual C++
* Watcom C/C++

从 BTR 文件中检索数据取决于与之关联的 DDF 文件。如果没有 DDF，就很难从这样的文件中检索信息。

## 参考

* [Btrieve - 维基百科](https://en.wikipedia.org/wiki/Btrieve)
* [Btreive API 简介](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

