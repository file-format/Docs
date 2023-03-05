{
  "date" : "2020-11-11",
  "keywords" :["ACCDB","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ACCDB 文件格式和可以创建和打开 ACCDB 文件的 API。",
  "title" :"ACCDB 文件格式 - Microsoft Access 2007 数据库文件",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## 什么是一 ACCDB 文件？

具有 .accdb 扩展名的文件是 Microsoft Access 2007 数据库文件，用于将用户数据存储在表中。支持收藏
自定义表单、SQL 查询和其他数据。在 Microsoft 转向基于 XML 的文件结构后，ACCDB 文件替换了 [MDB](/zh/database/mdb/) 文件。 ACCDB 文件仍然可以转换为具有旧兼容性的 MDB。但是，ACCDB 是现在广泛使用的 Access 数据库文件格式。 Microsoft 还支持 ACCDB 格式的附加功能，例如存储文件附件、二进制数据和多值字段支持的可能性。

## ACCDB 文件格式

与 MDB 一样，没有可用于 ACCDB 文件格式的公共规范。 Microsoft 支持通过开放式数据库连接 (ODBC) 标准和 Visual Basic for Applications (VBA) 以编程方式访问这些文件。

### 洞察力

一个简单的 ACCDB 文件的十六进制转储表明，在结构上与前身 MDB 格式系列的最新版本大体相似。两种文件格式都使用 4096 字节的固定页面大小。 ACCDB 和 MDB 的另一个相似之处是幻数的形式，其中包括 ACCDB 的字符串“Standard ACE DB"。版本或兼容性代码在两种格式中位于同一位置。 mdbtools | HACKING 文件指出“偏移 0x14 包含此数据库的 Jet 版本"并且非官方 MDB 指南同意。这些来源中的信息与 [Microsoft Jet 数据库引擎](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) 的 Wikipedia 条目相结合，表明值 0x02 表示 ACE 12 (Access 2007)，而 0x03 表示 ACE 14（访问 2010）。但是，在 Access 2010 中创建的最小数据库和在 Access 2016 中创建的类似数据库都在此位置具有 0x02。在 Access 2016 中创建的最小数据库，但定义了具有新引入的“大整数"数据类型的列，其值为 0x05。在 ACCDB 文件中，该指标似乎反映了文件的兼容性，而不是用于创建文件的 ACE 引擎的版本。

## 参考

* [访问文件格式](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Access 2016 规范](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet 数据库引擎](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [我应该使用哪种 Access 文件格式？](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
