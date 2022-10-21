{
  "date" : "2021-09-06",
  "keywords" :["adp","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","访问项目"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ADP 文件格式和可以创建和打开 ADP 文件的 API。",
  "title" :"ADP - 访问数据库文件",
  "linktitle" : "ADP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## 什么是一 .adp 文件？

具有 .adp 扩展名的文件是 Microsoft Access 项目文件，它使用 OLE DB 组件体系结构提供与 Microsoft SQL Server 数据库的直接有效连接。此类文件不包含实际的表格、数据库图表或其他数据库元素。可以使用 Access 2007 和 2010 创建 ADP 文件。使用早期版本的 Access 创建的文件也可以打开 Access 2007 和 2010。可以使用 Microsoft Access 365 打开 ADP 文件。

## ADP 文件格式 - 更多信息

作为 ADP 创建的 Access 项目允许您对 SQL 服务器对象（例如表和视图）进行设计更改。它还允许创建、编辑和利用 SQL 功能，例如数据库图表、存储过程和用户定义的函数。这比链接到无法更改设计并且只能链接到 SQL Server 表和视图的 SQL Server 数据库具有优势。

### 数据类型和图表支持

**日期/时间数据类型**

Access 2010 支持以下新的日期/时间数据类型。

* 时间
* 日期
* 日期时间2
* 日期时间偏移

**可变长度数据类型**

Access 2010 项目中可以使用以下可变长度数据类型：

* VARBIN（最大）
* VARCHAR(MAX)
* NVARCHAR(MAX)

## 参考

* [创建 Access 项目](https://support.microsoft.com/en-us/office/create-an-access-project-89c48da0-55a4-45d4-9ee5-95f67383d4cb)

