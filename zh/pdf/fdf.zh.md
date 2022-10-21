{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FDF 文件格式 - 什么是 FDF 文件？",
  "description":"了解 FDF 文件格式和可以创建和打开 FDF 文件的 API。",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .fdf 文件？

FDF（**Forms Data Format**）文件是通过从 [PDF](/zh/pdf/) 文件的表单域导出数据生成的文本文档。它仅包括从 PDF 文件中可用的表单字段中提取的文本字段数据。这导致数据文件相对较小，因为导出的数据不包含表单本身。 Adobe Acrobat 提供了通过使用应用程序菜单中的“导出表单数据"选项来导出表单字段数据的功能。

## FDF 文件格式 - 更多信息

FDF 是纯文本格式，是便携式文档格式 [ISO 32000 标准](https://www.iso.org/standard/51502.html) 的一部分。它由 Adobe 开发，允许从 Acrobat Forms 或 AcroForms 导入和导出数据。

FDF 文件有两种类型：

• `Classic FDF` – 它提供数据来填写现有的静态表格。

• `Template FDF` – 根据指定 PDF 文件中的模板构建新的 PDF。通过提供数据来填写新文档中的表格。

## 使用 Adobe Acrobat 创建 FDF

Adobe 的 [FDF 工具包](https://opensource.adobe.com/dc-acrobat-sdk-docs/) 允许您从文本数据创建 FDF 文件。

## 参考 ＃＃

* [Acrobat 支持的 FDF 格式](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assemble-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe 开发人员资源](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

