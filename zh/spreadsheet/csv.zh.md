{
  "date" : "2019-12-10",
  "keywords" :["CSV","文件","扩展名","文件格式","逗号分隔值","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 CSV 文件格式和可以创建和打开 CSV 文件的 API。",
  "title" :"CSV 文件格式",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是 .csv 文件？

具有 .csv（逗号分隔值）扩展名的文件表示纯文本文件，其中包含具有逗号分隔值的数据记录。 CSV 文件中的每一行都是文件中包含的记录集中的一条新记录。当数据从一个存储系统传输到另一个存储系统时，会生成此类文件。由于所有应用程序都可以识别以逗号分隔的记录，因此将此类数据文件导入数据库非常方便。几乎所有电子表格应用程序（例如 Microsoft Excel 或 OpenOffice Calc）都可以轻松导入 CSV。从这些文件导入的数据排列在电子表格的单元格中，以便向用户表示。

## 历史简介 ＃＃

以下是有关 CSV 文件格式的起源和历史的一些简要事实。

* 1972 - IBM Fortran（H 级扩展）编译器在 OS/360 下支持它们

* 1978 - FORTRAN 77 支持列表导向的输入/输出，它使用逗号和空格作为分隔符

* 2005 - CSV 被标准化为 [RFC4180](https://tools.ietf.org/html/rfc4180) 作为 MIME 内容类型。

* 2013 - RFC4180 的缺陷由 W3C 建议处理

* 2015 - W3C 为 CSV 元数据标准制定了建议的初稿，该建议于 2015 年 12 月开始作为建议

## 转换 CSV 文件 ##

使用可以打开这些文件的应用程序，可以将 CSV 文件转换为多种不同的文件格式。例如，Microsoft Excel 可以从 CSV 文件格式导入数据并保存到 XLS、[XLSX](/zh/spreadsheet/xlsx/)、[PDF](/zh/pdf/)、[TXT](/zh/word-processing/txt/) 、XML 和 [HTML](/zh/web/html/) 文件格式。同样，其他桌面和在线服务提供将 CSV 文件导出为 HTML、ODS 和 [RTF](/zh/word-processing/rtf/) 的功能。

## CSV 文件格式 ##

CSV 文件格式已知在 [RFC4180](https://tools.ietf.org/html/rfc4180) 下指定。在以下情况下，它将任何文件定义为符合 CSV 标准：

* 每条记录位于单独的行上，由换行符 (CRLF) 分隔。例如：
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* 文件中的最后一条记录可能有也可能没有结束换行符。例如：
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* 可能有一个可选的标题行出现在文件的第一行，格式与普通记录行相同。此标题将包含与文件中的字段对应的名称，并且应包含与文件其余部分中的记录相同数量的字段（标题行的存在或不存在应通过此选项的可选“header"参数指示MIME 类型）。例如：
* 字段名称，字段名称，字段名称 CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿在表头和每条记录中，可能有一个或多个字段，以逗号分隔。每一行都应在整个文件中包含相同数量的字段。空格被认为是字段的一部分，不应被忽略。记录中的最后一个字段后面不能有逗号。例如：
* aaa,bbb,ccc
* 每个字段可以用双引号括起来，也可以不用双引号（但是某些程序，例如 Microsoft Excel，根本不使用双引号）。如果字段没有用双引号括起来，则双引号可能不会出现在字段内。例如：\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* 包含换行符 (CRLF)、双引号和逗号的字段应该用双引号括起来。例如：
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* 如果使用双引号括住字段，则出现在字段内的双引号必须通过在其前面加上另一个双引号来进行转义。例如：
* "aaa","b""bb","ccc"

但是，根据现代用法，分隔符不仅限于逗号，还可以是分号、制表符或空格。 Microsoft Excel 等应用程序提供了用于指定从 CSV 文件导入记录的分隔符的选项。

## 参考

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - 维基百科](https://en.wikipedia.org/wiki/Comma-separated_values)

