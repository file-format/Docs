{
  "date" : "2020-11-11",
  "keywords" :["LDF","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 LDF 文件格式和可以创建和打开 LDF 文件的 API。",
  "title" :"LDF - SQL Server 主数据库文件格式",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .ldf 文件？

带有 .ldf 扩展名的文件是由 Microsoft SQL Server 维护的日志文件，它是一个关系数据库管理系统 (RDBMS)。在主数据库文件（[MDF](/zh/database/mdf/)）上执行的所有事务（例如插入、更新、删除）都记录在 LDF 文件中。 LDF 文件是任何数据库的关键组件。在系统故障的情况下，日志文件用于将数据库恢复到一致状态。如果事务未完全提交，事务日志文件的大小可能会增加。 LDF 文件可以使用 Microsoft SQL Server 软件应用程序打开。

## LDF 文件中记录的操作

SQL 日志文件记录以下操作：

* 每笔交易的开始和结束。

* 每次数据数据修改（插入、更新或删除）。这还包括系统存储过程或数据定义语言 (DDL) 语句对任何表（包括系统表）的更改。

* 每个范围和页面分配或释放。

* 创建或删除表或索引。

## LDF 文件格式

LDF 文件由排列为日志记录字符串的 SQL Server 事务记录组成。每条日志记录都有一个日志序列号 (LSN)，它高于前一条记录的 LSN。字符串在文件中彼此连接。由于现代高速计算机，可以在 LSN1 之前的日志文件中存在 LSN2 的位置插入记录。由于操作是串行记录的，因此 LSN2 描述的更改是在日志记录 LSN1 之后执行的。特定事务的记录使用使用的指针向后链接，并加速事务的回滚。
 

## 参考

* [数据库文件和文件组](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [事务日志架构和管理指南](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-服务器-ver15)

