{
  "date" : "2020-11-11",
  "keywords" :["MDF","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MDF 文件格式和可以创建和打开 MDF 文件的 API。",
  "title" :"MDF 文件格式 - SQL Server 主数据库文件",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .mdf 文件？

扩展名为 .mdf 的文件是 [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) 用于存储用户数据的主数据库文件。这是最重要的，因为所有数据都存储在此文件中。 MDF 文件以列、行、字段、索引、视图和表的形式将用户数据存储在关系数据库中。 SQL Server 允许设置自动增长和自动收缩设置以对数据库的性能产生积极影响。可以使用 Microsoft SQL Server 加载 MDF 文件并将其附加到数据库。 MDF 文件具有 Application/octet-stream mime 类型。

## 中密度纤维板文件格式

SQL Server 中数据存储的基本单位是页面。数据库分配的存储页被划分为从 0 到 n 编号的逻辑页。单个页面以 96 字节的标题开始，其中包括页面 ID、页面所属的结构类型、页面中的记录数以及指向上一页和下一页的指针。

### 文件结构

MDF 文件具有以下数据结构。

* 第 0 页：页眉
* 第 1 页：第一个 PFS
* 第 2 页：第一个 GAM
* 第 3 页：第一个 SGAM
* 第 4 页：未使用
* 第 5 页：未使用
* 第 6 页：第一个 DCM
* 第 7 页：第一个 BCM

#### 文件头

所有文件的页码 0 包含一个标题，该标题存储有关文件的元数据。

#### 页面可用空间 (PFS)
PFS 识别分配状态并确定可用空间量。

* Bit 1：表示页面是否被分配。
* 位 2：指示页面是否来自混合范围。
* Bit 3：表示该页面是IAM页面。
* Bit 4：表示此页面包含幽灵记录
* 位 5 到 7：组合的三位值，表示页面充满度，如下所示：
* 0：页面为空
* 1：页面已满 1–50%
* 2：页面已满 51–80%
* 3：页面已满 81–95%
* 4：页面已满 96–100%

## 参考

* [数据库文件和文件组](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [数据库分离和附加 - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [分析SQL Server数据文件解剖](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

