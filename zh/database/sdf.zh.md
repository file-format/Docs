{
  "date" : "2021-05-03",
  "keywords" :[ "SDF","sdf 文件","什么是 sdf 文件","如何打开 sdf 文件","扩展名","文件","sdf 文件格式","数据库文件类型","数据库文件格式", "数据库文件" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 SDF 文件格式和可以创建和打开 SDF 文件的 API。",
  "title" :"SDF - SQL Server 紧凑型数据库文件",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## 什么是一 .sdf 文件？
扩展名为 .sdf 的文件包含 Microsoft SQL Server Compact (SQL CE) 数据库，也称为紧凑型关系数据库；微软为移动设备和桌面应用程序制作的。它支持 32 位和 64 位操作系统，数据库的全部内容包含在单个 SDF 文件中，可占用 4GB 以上的磁盘空间。出于安全目的，可以使用 128 位加密对 .sdf 文件进行加密。 SQL CE 运行时解决了对 .sdf 文件的并行多用户访问。 SDF 文件可以通过 **QuickOnce** 复制，也可以简单地复制到目标位置以进行系统部署。

## SDF 文件格式
SDF 文件包含一个通常称为紧凑关系数据库的数据库。 SDF 文件包含所有与数据库相关的信息，SQL Server Compact 是一个轻量级且免费的数据库引擎，用于管理 .sdf 文件。 .sdf 文件大小不应超过 4 GB 大小的限制。 SDF 文件不存储有关存储过程、触发器或视图的信息。使用 SQL CE 数据库的应用程序无需在 ADO.NET 连接字符串中指定 SDF 文件的路径，而是可以将其称为 |DataDirectory|\database_name.sdf，定义在程序集清单中为应用程序定义的数据目录
.sdf 命名约定是可选的，可以使用任何扩展名来保存文件。为数据库文件设置密码是可选步骤。要压缩或修复数据库，应使用 **compacted/repaired database** 选项保存文件。

## 参考

* [SQL Server Compact - 维基百科](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [将 SQL Server Compact 用于 ASP.NET Web 应用程序](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


