{
  "date" : "2020-11-11",
  "keywords" :["NDF","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MDF 文件格式和可以创建和打开 NDF 文件的 API。",
  "title" :"NDF 文件格式 - SQL Server 主数据库文件",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .ndf 文件？

带有 .ndf 扩展名的文件是 [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) 用于存储用户数据的辅助数据库文件。 NDF 是辅助存储文件，因为 SQL Server 将用户指定的数据存储在称为 [MDF](/zh/database/mdf/) 的主存储文件中。 NDF 数据文件是可选的，并且是用户定义的，用于管理数据存储，以防主 MDF 文件使用所有分配的空间。它通常存储在单独的磁盘上，并且可以传播到多个存储设备。为了打开 NDF 文件，MDF 文件的存在是必要的。

## NDF 文件格式

NDF 文件格式与 [MDF](/zh/database/mdf/) 没有什么不同，并且使用页面作为数据存储的基本单元。每页以 96 字节的标头开头，其中包括：

* 页面编号
* 结构类型
* 页面中的记录数
* 指向上一页和下一页的指针

### NDF 文件结构

MDF 文件具有以下数据结构。

* 第 0 页：页眉
* 第 1 页：第一个 PFS
* 第 2 页：第一个 GAM
* 第 3 页：第一个 SGAM
* 第 4 页：未使用
* 第 5 页：未使用
* 第 6 页：第一个 DCM
* 第 7 页：第一个 BCM

#### NDF 文件头

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

## 数据文件页面

SQL Server 数据文件中的页面从零 (0) 开始并按顺序递增。每个文件都由一个唯一的文件 ID 号识别。文件 ID 和页码对唯一地标识数据库中的页面。显示数据库中页码的示例如下图所示。

{{< figure src="../ndf.png" alt="NDF 数据库文件格式" >}}

此示例显示具有 4 MB 主数据文件和 1 MB 辅助数据文件的数据库中的页码。

## 参考

* [数据库文件和文件组](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [数据库分离和附加 - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [分析SQL Server数据文件解剖](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

