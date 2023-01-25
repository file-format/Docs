{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODTTF 文件 - 混淆的 OpenType 字体文件格式”，
  "description":"了解 ODTTF 文件格式和可以创建和打开 ODTTF 文件的 API。”,
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## .ODTTF 文件是什么？

ODTTF 文件是 [.XPS](/zh/page-description-language/xps/) 和 Microsoft Office 2007 文件格式使用的字体文件格式。它包含经过修改的混淆 OpenType 字体，以便难以提取字体的设计信息或对字体的源代码进行逆向工程。 ODTTF是基于原始文档中使用的字体，但不是纯格式，可能无法被第三方软件读取以提取字体数据。

您可以使用 Pagemark XpsViewer、带有 Pagemark XpsPlugin 的 Apple Safari、带有 Pagemark XpsPlugin 的 Mozilla Firefox 打开 ODTTF 文件，
NiXPS 查看和 NiXPS 编辑。

## ODTTF文件格式

ODTTF 文件格式的内部文件格式结构是未知的，因为它们存储为嵌入式混淆格式。这些可以嵌入到数字文档中，例如 .PDF 或 .DOCX。

## 参考
* [Microsoft 的 OpenType 字体规范](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType 概述](https://docs.microsoft.com/en-us/typography/truetype/)

