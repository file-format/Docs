{
  "date" : "2021-08-24",
  "keywords" :["wdb 文件","wdb 文件格式","什么是 wdb 文件","文件","wdb 示例","wdb 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 WDB 文件格式和可以创建和打开 WDB 文件的 API。",
  "title" :"WDB - SQL Server 跟踪文件",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是一 .wdb 文件？
扩展名为 .wdb 的文件实际上是由 Microsoft Works 创建的数据库文件，用于执行数据库管理系统等功能。 WDB 文件类似于 Access 数据库 ([MDB](/zh/database/mdb/)) 文件，但效率较低且限制较大。无法使用 Microsoft Access 打开 WDB 文件。但是，您可以在 Microsoft Works 中打开 WDB 文件，然后将其导出为 MDB 文件，以便在 MS Access 中打开 WDB 文件。

## WDB 文件格式
Microsoft Works 数据库是 Microsoft Works 办公套件的本机数据库格式。由于格式的专有性质和一些限制。 WDB 文件不能在 Microsoft Works 以外的任何其他软件中打开。在文件格式中，可以在每个 ASCII 文本字符串之前找到一个重复出现的 10 字节标题，这些字符串表示由 NULL 值终止的字段的值。标头通常以 **\x0f** 字节和 NULL 开头，然后是 4 个数据字节与 NULL 交替。

### 文件结构

WDB文件的结构如下：
- **第一个标头**：从文件的开头开始，以 \x25\x00\xf2 和 244 个 NULL 字节结尾
- **第二个标题**：以 \xffT 开头 - 即 \xff\x54 并扩展为 4096 个字节，其中包含列/字段名称和其他内容，并且似乎从字节位置 6144 开始。
- **字段**：值有一个 10 字节的标头，格式如下：{type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 ，第 2 部分} {db 4} \x00。数据字节 2 是字段号，数据字节 3 是记录号（添加数据字节 3，超过 256 条记录时的第 2 部分）。


## 参考 ＃＃

* [用户:JesseW/wdb 格式](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

