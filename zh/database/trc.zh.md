{
  "date" : "2021-08-24",
  "keywords" :["trc 文件","trc 文件格式","什么是 trc 文件","文件","trc 示例","trc 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 TRC 文件格式和可以创建和打开 TRC 文件的 API。",
  "title" :"TRC - SQL Server 跟踪文件",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是一 .trc 文件？
具有 .trc 扩展名的文件包含 Miscrosoft SQL Server 数据库活动的跟踪结果。这些文件由软件 SQL Server Profiler 创建；通常与 Microsoft SQL Server 软件一起打包。数据库管理员可以分析一系列数据库语句，如果怀疑有某种错误或警告，可以查看跟踪日志。这些文件通常位于 Windows 操作系统的 Program Files 目录内的 MSSQL 的典型 LOG 文件夹中。

## TRC 文件格式
SQL Server Profiler 使用 TRC 文件格式自动生成 MS SQL 服务器最近执行的语句的新跟踪。 SQL Server Profiler 对任何新跟踪都使用默认模板。但是，该软件包含几个预定义的模板，用于监控某些类型的事件。 SQL Server Profiler 还可用于创建模板，这些模板定义要包含在跟踪中的事件类和数据列。

### 预定义模板
以下是 SQL Server Profiler 中包含的一些预定义模板的列表：
- **SP_Counts**：随着时间的推移捕获存储过程的执行行为。
- **标准**：创建跟踪的通用起点。
- **TSQL**：捕获客户端提交给 SQL Server 的所有 Transact-SQL 语句和发出的时间。
- **TSQL_Duration**：捕获客户端提交给 SQL Server 的所有 Transact-SQL 语句、它们的执行时间，并按持续时间对它们进行分组。
- **TSQL_Grouped**：用于调查来自特定客户端或用户的查询。
- **TSQL_Locks**：用于解决死锁、锁定超时和锁定升级事件。
- **TSQL_Replay**：用于执行迭代调优，例如基准测试。
- **TSQL_SPs**：用于分析存储过程的组件步骤。
- **Tuning**：用于生成跟踪输出，数据库引擎优化顾问可以将其用作工作负载来优化数据库。
### 将跟踪与 Windows 性能日志数据相关联
SQL Server Profiler 可用于打开 Microsoft Windows 性能日志，选择与跟踪相关的计数器，并在 MS SQL Server Profiler GUI 中的跟踪旁边显示选定的性能计数器。为了指示与所选跟踪事件相关的性能日志数据，SQL Server Profiler 的系统监视器数据窗口窗格中的垂直红色条。


## 参考 ＃＃

* [SQL Server Profiler](https://docs.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

