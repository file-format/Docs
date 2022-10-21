{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF 文件格式 - 什么是 XFDF 文件？",
  "description":"了解 XFDF 文件和可以创建和打开 XFDF 文件的 API。",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .xfdf 文件？

带有 .xfdf 扩展名的文件是使用 Adobe Acrobat 软件生成的 XML 表单数据格式。与 [FDF](/zh/pdf/fdf/) 类似，XFDF 包含 XML 格式的表单元素描述及其值。这可以包括 PDF 表单中文本字段的名称和值。 XFDF 以人类可读的格式保存，并且可以使用 C# 等编程语言以编程方式读取。

## XFDF 文件格式 - 更多信息

XFDF 文件以 XML 文件格式保存，该格式是用于导入和导出数据的通用格式。 XFDF 文件结构由标题、字段值和元素数据组成，如下所示。

|元素|属性|内容|
---|---|---|
|\<XFDF> ||最顶层元素|
|\<fields> ||此模板的所有字段值|
|<field (T)> |名称 |字段名称|
|<value (V)> |值 |字段值|

## 参考

* [Acrobat 支持的 FDF 格式](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assemble-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe 开发人员资源](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

