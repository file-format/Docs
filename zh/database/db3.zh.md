{
  "date" : "2019-12-12",
  "keywords" :["DB3","DB3 文件格式","DB3 文件","SQLite","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DB3 文件格式和可以创建和打开 DB3 文件的 API。",
  "title" :"DB3 文件格式",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## 什么是 DB3 文件？
DB3 文件是由 SQLite 软件创建的数据库文件，该软件是一个轻量级,自包含的数据库程序，它使用纯文件创建数据库；包含数据库结构以及数据记录；通常用于使用 SQL 检索或存储结构化数据。这些文件可用于智能设备或需要记录保存或其他数据管理但空间较小的环境中。


## DB3 文件格式
DB3 文件格式与 RDBMS（关系数据库管理系统）SQLite 相关联，后者是嵌入式数据库的流行选择。 SQLite_3 在其规范中没有定义任何特定的文件扩展名，它可以使用包括 [.dbf](/zh/database/dbf/) 和 [.sqlite](/zh/database/sqlite/) 的扩展名。

### 数据库规范
通常 SQLite，版本 3 相关的 db 文件格式可以被认为是自 2004 年 6 月以来用作 SQLite 数据库引擎公开记录的原生格式的 DB3 文件格式。DB3 文件格式是一种跨平台，可在 big-endian 之间传输和 little-endian 架构或 32 位和 64 位系统。这些特性使 DB3 成为一种流行的应用程序文件格式选择。主 SQLite_3 数据库 (DB3) 文件由一页或多页组成。在同一个数据库中，所有页面的所有大小都相等。页面大小（以字节为单位）是 512 到 65536（含）之间的 2 的幂。



## 参考 ＃＃

* [SQLite - 维基百科](https://en.wikipedia.org/wiki/SQLite)
* [SQLite，版本 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)

