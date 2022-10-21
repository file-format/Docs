{
  "date" : "2020-11-11",
  "keywords" :["BCP","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 BCP 文件格式和可以创建和打开 BCP 文件的 API。",
  "title" :"BCP - SQL Server 大容量复制文件格式",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .bcp 文件？

BCP（批量复制格式）是 Microsoft SQL Server 的技术数据格式，它定义数据结构以存储不同的数据库数据类型值以进行导入/导出。该格式完全定义了每个数据列的解释，以便可以读取数据文件中指定的一组值。 [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) 实用程序使用 BCP 文件格式读取来自此类文件的数据并识别它。


## BCP 文件格式

BCP 格式文件是定义列顺序、名称和数据类型的 XML 文档。它允许用户从指定这些字段的数据文件中导入/导出大量数据。这有助于从数据文件中批量导入数据值。数据文件中数据字段的数量和顺序可能与目标表列中的不同。这是 BCP 数据格式文件通过指定用于导入数据的列的顺序和类型来提供帮助的时候。

格式文件的结构用以下格式表示。

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP 数据类型

|数据类型|范围|表示|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) 到 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|二进制|1 到 8000 字节|十六进制编码的 Unicode 字符串格式 `Binary = 32000OCTET`|
|Bit|0 或 1|简单的 Unicode 字符串 Bit = "0" / "1"|
|Char|1 到 8000|Unicode 字符串格式，Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET 其中 n = 4 x (2,147,483,647)|
|日期|0001-01-01 到 9999-12-31|YYYY-MM-DD 字符串格式|
|日期时间|1753-01-01 00:00:00.000 到 9999-12-31 23:59:59.997| Unicode YYYY-MM-DD hh:mm:ss[.nnn] 字符串格式|
|DateTime2|0001-01-01 00:00:00.0000000 到 9999-12-31 23:59:59.9999999。| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] 字符串格式|
|DateTimeOffset|协调世界时 (UTC) 时区的 0001-01-01 00:00:00.0000000 到 9999-12-31 23:59:59.9999999| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] 字符串格式|
|十进制|-1038 + 1 到 1038 – 1|Unicode 字符串格式 `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|浮点数|-1.79E+308 到 -2.23E-308； 0;从 2.23E-308 到 1.79E+308|Unicode 字符串格式|
|图像|范围从 0 到 231 – 1 (2,147,483,647)的字节序列|十六进制编码的 Unicode 字符串格式|
|Int|-231 (-2,147,483,648) 到 231 – 1 (2,147,483,647)|Unicode 字符串格式|

## 参考

* [BCP 格式 - 微软](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

