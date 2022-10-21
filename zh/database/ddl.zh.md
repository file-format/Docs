{
  "date" : "2020-11-11",
  "keywords" :["DDL","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DDL 文件格式和可以创建和打开 DDL 文件的 API。",
  "title" :"DDL 文件格式 - 数据定义语言文件",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## 什么是一 .ddl 文件？

扩展名为 .ddl 的文件是一种数据定义语言文件，用于定义数据库的架构。它包含用于处理数据库结构（例如表、列、记录和其他字段）的语句/命令。 DDL 文件中的命令是用 [SQL](/zh/database/sql/) 编写的，可以执行在数据库中创建表、删除和更新等操作。数据库模式归其创建者所有，并且可以在其上执行所有 CRUD 操作。可以创建和打开 DDL 文件的流行应用程序是 Windows 文本编辑器、Jetbrains Intellij Idea 和 EclipseLink。

## DDL 命令

单个 DDL 文件可以包含多个命令，由于语法正确，这些命令将按顺序执行并对模式进行更改，例如创建字符集和表、删除表、重命名和更改表。在使用数据库模式时，通常使用以下 DDL 命令。

`CREATE` - 用于创建数据库或其对象（如表、索引、函数、视图、存储过程和触发器）。

`DROP` - 用于从数据库中删除对象。

`ALTER` - 用于改变数据库的结构。

`TRUNCATE` - 用于从表中删除所有记录，包括删除为记录分配的所有空间。

`COMMENT` - 向数据字典添加评论。

`RENAME` - 重命名数据库中的现有对象。

## DDL 示例

以下示例显示了用于创建表并定义其字段的 CREATE 命令的 DDL 语句。

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## 参考 ＃＃

* [维基百科的 DDL](https://en.wikipedia.org/wiki/Data_definition_language)

