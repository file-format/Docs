{
  "date" : "2020-11-11",
  "keywords" :["ACCDT","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ACCDT 文件格式和可以创建和打开 ACCDT 文件的 API。",
  "title" :"ACCDT - Microsoft Access 2007 模板数据库文件格式",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## 什么是一 ACCDT 文件？

带有 .accdt 扩展名的文件是一个 Microsoft Access 数据库模板文件，其中包含预定义的数据库元素。这些元素是定义数据库应用程序的结构的集合，例如用于存储数据的数据库模式、数据视图的布局描述以及描述数据库的元数据。作为模板文件，ACCDT 文件可用于根据其中可用的模板设置创建数据库。生成的数据库文件保存为 [ACCDB](/zh/database/accdb/) 文件，并在表格中填充数据。 Microsoft Access 2007 及更高版本可以打开 ACCDT 文件。

## ACCDT 文件格式

ACCDT 模板文件基于 Office Open XML 规范，所有数据都包含在 ZIP 包中。数据库的结构和内容信息包含在[XML](/zh/web/xml/) 文件和文本文件中，并通过关系相互链接。您可以将 ACCDT 文件重命名为 [.zip](/zh/compression/zip/) 扩展名，并使用任何压缩软件来提取 ZIP 存档的内容。

### 文件结构

ACCDT 文件是包含相关部分集合的包。每个**部分**使用 XML、文本和二进制格式存储有关数据库应用程序内容的信息，包括：

* 数据库对象
* 相关元数据
* 包的结构

＃＃＃＃ 包裹

包是一个 [ZIP](/zh/compression/zip/) 存档，包含多个部分并符合 [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html)。 ACCDT 文件必须包含至少一个模板元数据部分，它应该是关系的目标。此模板元数据是 ACCDT 文件的起始部分。

＃＃＃＃ 部分

一个部分是一个字节流，它具有一个关联类型，用于指定存储在其中的内容的性质和类型。部件枚举指定包中所有部件之间的有效部件、有效内容类型和所需关系。

＃＃＃＃ 关系

`包关系` - 其中目标是一部分，源是整个包。

`零件到零件的关系` - 目标是零件，源是包中的零件。

`显式关系` - 通过其 ID 属性的值引用关系元素，从源部分的内容中引用资源。

`隐式关系` - 一种不显式的关系。

`内部关系` - 目标是包中的一部分。

`外部关系` - 目标是不在包中的外部资源。

## 参考 ＃＃

* [访问模板文件格式](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

