{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - 报告定义语言文件",
  "keywords" :["rdl","报告定义语言","XmlTextWriter","XSD","RDL 元素"],
  "description":"了解 RDL 文件格式,它是 SQL Server Reporting Services 报告定义的 XML 表示形式。",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## 什么是一 .rdl 文件？ ##

RDL（报表定义语言）是 Microsoft 为定义报表而设置的基准。一个 RDL 文件由一个或多个 RDL 元素组成。而 RDL 元素由其数据类型和基数组成。一个元素可以是简单的或复杂的。简单元素没有任何子元素或属性，而复杂元素有子元素和可选属性。

## RDL XML 模式定义
XML 架构定义 (XSD) 文件验证 RDL 文件。架构定义了 RDL 元素可以在 .rdl 文件中出现的位置的规则。 RDL 元素可以是简单的也可以是复杂的。简单元素没有子元素或属性，而复杂元素确实有子元素和可选的属性。

## 创建 RDL
由于 RDL 本质上是开放且可扩展的，因此可以构建许多基于其 XML 模式生成 RDL 文件的应用程序和工具。从应用程序创建 RDL 的最简单方法之一是使用 **System.Xml** 命名空间和 System.Linq 命名空间的 Microsoft .NET Framework 类。特别是 **XmlTextWriter** 类，可用于编写 RDL。您可以使用 **XmlTextWriter** 在任何 .NET Framework 应用程序中从头到尾生成完整的报表定义。开发人员还可以添加具有自定义属性的自定义报表项来扩展 RDL。

## RDL 类型
下表列出了 RDL 元素中使用的类型和属性。

|类型|描述|
---|---|
|二进制 |具有 base-64 编码二进制值的属性。|
|布尔|以 true 或 false 作为对象值的属性。除非另有说明，否则省略的可选布尔对象的值为 False。|
|日期 |具有以 ISO8601 日期格式指定的完全指定日期或日期时间值的属性：YYYY-MM-DD[THH:MM[:SS[.S]]]。|
|枚举 |具有必须是指定值列表之一的字符串文本值的属性。|
|Float |具有浮点值的属性。句点 (.) 用作可选的小数分隔符。|
|整数 |具有整数 (int32) 值的属性。|
|语言 |具有包含语言和文化代码的文本值的属性，例如美国英语的“en-us"。该值必须是特定语言或在 Microsoft .NET Framework 中为其定义默认语言的中性语言。
|名称 |具有字符串文本值的属性。名称在项目的命名空间中必须是唯一的。如果未指定，则项目的命名空间是具有名称的最里面的包含对象。
|NormalizedString |具有已规范化的字符串文本值的属性。|
|大小 |大小元素必须包含一个数字（使用句点字符作为可选的小数分隔符）。数字后面必须跟 CSS 长度单位的指示符，例如 cm、mm、in、pt 或 pc。数字和代号之间的空格是可选的。有关尺寸指示符的更多信息，请参阅 CSS 值和单位参考。在 RDL 中，尺寸的最大值为 160 英寸。最小尺寸为 0 英寸。|
|String |具有字符串文本值的属性。|
|UnsignedInt |具有无符号整数 (uint32) 值的属性。|
|变体 |具有任何简单 XML 类型的属性。|

## RDL 数据类型
在 RDL 中，DataType Enumeration 定义属性、表达式或参数的数据类型。下表显示了 CLR 数据类型与 RDL 数据类型的对应关系。

|CLR 类型 |对应的数据类型|
---|---|
|布尔|布尔|
|日期时间、日期时间偏移 |日期时间|
|Int16、Int32、UInt16、字节、SByte |整数|
|单、双 |浮动|
|字符串、字符、GUID、时间跨度 |字符串|


## 参考 ＃＃

- [报告定义语言（维基百科）]（https://en.wikipedia.org/wiki/Report_Definition_Language）
- [报告定义语言 (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

