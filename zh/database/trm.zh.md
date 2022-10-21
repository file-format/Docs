{
  "date" : "2022-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 TRM 文件格式和可以创建和打开 TRM 文件的 API。",
  "title" :"TRM 文件格式 - Oracle 跟踪映射文件",
  "linktitle" : "TRM",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是 Oracle TRM 文件？

TRM 文件是 Oracle 11g 关系数据库管理系统 (RDBMS) 使用的元数据文件格式。它与 Oracle 跟踪文件 ([.trc](/zh/database/trc/)) 一起存储，并包含有关跟踪文件的结构信息。 TRM 文件的目的是便于使用元数据信息搜索和导航记录。 Oracle 软件可用于打开 TRM 文件。

## TRM 文件格式

TRM 文件以 Oracle 的专有文件格式保存，TRM 文件格式详细信息不公开。典型的 TRC 文件包含 Oracle 进程 SID、进程名称和 OS 进程号。 TRM 文件包含有关这些 TRC 文件的详细元数据信息，用于搜索和导航。

## 参考 ＃＃

* [oracle 11g 中的 .trm 文件是什么？](https://community.oracle.com/tech/developers/discussion/945615/what-is-trm-file-in-oracle-11g)

