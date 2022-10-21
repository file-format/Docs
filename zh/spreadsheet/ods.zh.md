{
  "date" : "2019-12-10",
  "keywords" :["ODS","文件","扩展名","文件格式","OpenDocument 电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南,了解什么是 ODS 文件以及可以创建和打开它们的 API。",
  "title" :"什么是 ODS 文件？",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是一 .ods 文件？

带有 .ods 扩展名的文件代表用户可编辑的 OpenDocument 电子表格文档格式。数据在 ODF 文件中存储为行和列。它是基于 XML 的格式，是开放文档格式 (ODF) 系列中的几个子类型之一。该格式被指定为 OASIS 发布和维护的 ODF 1.2 规范的一部分。 Windows 和其他操作系统上的许多应用程序可以打开 ODS 文件进行编辑和操作，包括 Microsoft Excel、NeoOffice 和 LibreOffice。 ODS 文件也可以通过不同的应用程序转换为其他电子表格格式，如 [XLS](/zh/spreadsheet/xls/)、[XLSX](/zh/spreadsheet/xlsx/) 等。

## 历史简介 ＃＃

ODS 文件格式规范基于作为 ODF 规范开发的标准。这些规范在过去以三个版本的形式演变，由 OASIS 开发和发布，如下所示：

`2005`- 1.0 版于 2005 年 5 月发布

`2007` - 1.1 版于 2007 年 2 月发布

`2011` - 1.2 版于 2011 年 9 月发布

从 ODF 1.0 到 1.1 版本的转换有相当小的变化。 【ODF 1.2版本】(https://www.oasis-open.org/standards#opendocumentv1.2)是ODF规范的最新版本，开发者开发ODS读/写相关的应用，请参考。

## ODS 文件格式 ##

OpenDocument 格式支持将文档表示为单个 XML 文档以及作为 [ZIP](/zh/compression/zip/) 存档的包中的多个子文档的集合。 ZIP 存档中的每个文件都存储了完整文档的一部分。每个子文档存储文档的特定方面。例如，一个子文档包含样式信息，而另一个子文档包含文档的内容。典型的 ODF 文档具有以下组件：

* `content.xml` - 文档内容和内容中使用的自动样式。
* `styles.xml` - 文档内容中使用的样式和样式本身中使用的自动样式。
* `meta.xml` - 文档元信息，例如作者或上次保存操作的时间。
* `settings.xml` – 特定于应用程序的设置，例如窗口大小或打印机信息。

除此之外，包中还可以包含许多其他子文档，例如文档缩略图、图像等。

电子表格文档文件是 ODF 文件的子集，其中内容（表格）存储在 content.xml 子文档中。

## 参考 ＃＃

* [OpenDocument - 维基百科提供](https://en.wikipedia.org/wiki/OpenDocument)

