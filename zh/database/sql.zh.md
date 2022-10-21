{
  "date" : "2020-11-11",
  "keywords" :["SQL","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 SQL 文件格式和可以创建和打开 SQL 文件的 API。",
  "title" :"SQL 文件格式 - 结构化查询语言数据文件",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## 什么是 SQL 文件？

带有 .sql 扩展名的文件是结构化查询语言 (SQL) 文件，其中包含使用关系数据库的代码。它用于为数据库上的 CRUD（创建、读取、更新和删除）操作编写 SQL 语句。 SQL 文件在使用桌面和基于 Web 的数据库时很常见。 SQL 有多种替代方案，例如 Java 持久性查询语言 (JPQL)、LINQ、HTSQL、4D QL 和其他几种。 SQL 文件可以通过 Microsoft SQL Server、MySQL 的查询编辑器和其他纯文本编辑器（如 Windows 操作系统上的记事本）打开。

## 历史简介

* 由 IBM 的 Donal D. Chamberlin 和 Raymond F. Boyce 于 1970 年代初开发和推出
* 用于存储和检索 IBM 原始准关系数据库管理系统 System R 中的数据
* 开始在商业产品基础上使用他们的 System R 原型，包括 System/38、SQL/DS 和 DB2，它们分别于 1979 年、1981 年和 1983 年上市。
* 1986 年被 ANSI 和 ISO 标准组正式采用为关系数据库管理系统 (RDBMS) 的标准“数据库语言 SQL"

## SQL 文件格式

SQL 文件是纯文本格式，可以包含多种语言元素。如果可以在不相互依赖的情况下执行多个语句，则可以将多个语句添加到单个 SQL 文件中。这些 SQL 命令可以由查询编辑器执行以执行 CRUD 操作。

### SQL 语言元素

SQL 语言元素如下所列。

|元素|描述|
---|---|
|条款|语句和查询的组成部分。|
|表达式|可以生成标量值或由数据列和行组成的表|
|谓词|指定可以评估为 SQL 三值逻辑 (3VL)（真/假/未知）或布尔真值的条件，用于限制语句和查询的效果，或更改程序流程。|
|查询|根据特定标准检索数据。这是 SQL 的一个重要元素。|
|声明|可能对模式和数据产生持久影响，或者可能控制事务、程序流、连接、会话或诊断。|

### SQL 示例
下面的 SQL 语句创建了一个名为 **DATA** 的表，然后是附加的 `INSERT` 命令以在该表中插入记录。
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## 参考 ＃＃

* [维基百科的 SQL](https://en.wikipedia.org/wiki/SQL)
* [SQL 语法](https://en.wikipedia.org/wiki/SQL_syntax)

