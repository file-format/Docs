{
  "date" : "2023-01-16",
  "keywords" :[ "DB-WAL", "什么是 DB-WAL 文件", "扩展名", "文件", "文件格式", "数据库文件类型", "数据库文件格式", "数据库文件" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DB-WAL 文件格式和可以创建和打开 DB-WAL 文件的 API。",
  "title" :"DB-WAL 文件格式 - SQLite 数据库预写日志文件",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## 什么是 DB-WAL 文件？

文件扩展名 .db-wal 与 SQLite 相关联，SQLite 是一种流行的开源关系数据库管理系统。 WAL 文件格式（Write-Ahead Log 的缩写）是 SQLite 使用的传统回滚日志的替代方案。它提供了更多的并发控制，允许多个进程同时读取数据库，同时仍然提供崩溃恢复能力。 .db-wal 文件用于存储对数据库所做的更改，这些更改尚未提交到主数据库文件（扩展名为 .db）。

## 通用 WAL 格式

在 WAL（Write-Ahead Log）文件格式中，对数据库所做的更改首先写入 WAL 文件，然后再提交到主数据库文件。这允许对数据库进行更多并发访问，因为多个进程可以在进行更改时从数据库中读取。此外，WAL 文件格式提供崩溃恢复功能，允许数据库在意外关闭时回滚到以前的状态。

## DB-WAL 和 WAL 格式的区别

.db-wal 和 WAL 文件格式都与 SQLite 相关联，SQLite 是一种流行的开源关系数据库管理系统。但是，两者之间存在细微差别。

.db-wal 文件本质上是一个 WAL 文件，但具有不同的文件扩展名。 .db-wal文件用于存储对数据库所做的尚未提交到主数据库文件（扩展名为.db）的更改，而WAL文件格式用于存储数据库更改的预写日志.

换句话说，.db-wal 文件是一种特定类型的 WAL 文件，SQLite 数据库使用它来存储对数据库所做的尚未提交到主数据库文件的更改。 WAL文件格式是这类文件格式的总称。

所以，WAL是文件格式的总称，.db-wal是SQLite数据库使用的WAL文件格式的具体实现。

## 参考
* [WAL 模式文件格式](https://www.sqlite.org/walformat.html)
* [预写日志记录](https://www.sqlite.org/wal.html)

