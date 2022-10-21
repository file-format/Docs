{
  "date" : "2020-11-11",
  "keywords" :["MDB","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MDB 文件格式和可以创建和打开 MDB 文件的 API。",
  "title" :"MDB 文件格式 - Microsoft Access 数据库文件",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## 什么是一 .mdb 文件？

扩展名为 .mdb 的文件是 Microsoft Access 数据库文件，它是一个关系数据库管理系统 (RDBMS)。它将数据存储在通过主键和外键相互链接的数据库表中。 MDB 文件包含数据库表、查询、存储过程的完整结构。 MDB 是 Microsoft Access 2003 的默认文件格式。Microsoft Access 的横向版本使用 [ACCDB](/zh/database/accdb/) 文件格式，这是迄今为止最新的文件格式。 MDB 文件可以使用 Microsoft Access、MDB Viewer、MDBOpener 等应用程序打开，并且可以转换为 ACCDB、[CSV](/zh/spreadsheet/csv/)、Excel 格式等。

## MDB 文件格式

MDB 格式有可用的公共规范，它仍然是 Microsoft 的专有文件格式。但是，Microsoft 使用开放式数据库连接 (ODBC) 标准和 Visual Basic for Applications (VBA) 提供对 MDB 文件的连接访问。非官方的 MDB 指南提供了基于逆向工程的 MDB 格式的简短非正式描述，可以查阅以了解规范。

### 页

根据非官方 MDB 指南，MDB 文件由固定大小的页面组成（Jeb DB3 为 2048 字节，Jet DB 4 为 4096 字节）。第一个字节表示页面的类型。以下是关键页面类型：

`First Page:` 它包含数据库标头信息，其中还包括与文件兼容的 Jet DB 版本的标识。此外，它还包括文件安全信息和页面使用图。

`表定义页面：`表定义页面指定列、数据类型、索引和其他信息。如果需要，它会使用其他页面，并包含一个包含此表的行数据的页面映射。

`数据页：`数据页是按行存储数据的实际数据容器。它使用辅助页面来存储长数据值。

单个 Microsoft Access 数据库可能包含多个允许超出文件和表大小限制的文件。这有助于将表单和代码放在用户桌面上的前端 MDB 文件中，并将数据放在连接到网络的服务器上的另一个后端 MDB 文件中。

## 参考 ＃＃

* [访问规范](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [非官方 MDB 指南](http://jabakobob.net/mdb/)

