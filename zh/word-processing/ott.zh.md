{
  "date" : "2019-10-11",
  "keywords" :["ott 文件","ott 文件格式","什么是 ott 文件","文件","ott 示例","ott 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - OpenDocument 模板文件",
  "description":"了解 OTT 文件格式和可以创建和打开 OTT 文件的 API。",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ott 文件？

带有 OTT 扩展名的文件表示由应用程序生成的符合 OASIS 的 OpenDocument 标准格式的模板文档。这些是使用免费的 OpenOffice Writer 等文字处理器应用程序创建的，并且可以保存可用于从这些模板文件生成新文档的设置。这些设置包括页边距、边框、页眉、页脚和其他页面设置。此类模板用于公司信头和标准化表格等官方文件。

## 历史简介 ＃＃

ODP 文件格式规范基于作为 ODF 规范开发的标准。这些规范在过去以三个版本的形式演变，由 OASIS 开发和发布，如下所示：

**2005：** 1.0 版于 2005 年 5 月发布

**2007：** 1.1 版于 2007 年 2 月发布

**2011：** 1.2 版于 2011 年 9 月发布

从 ODF 1.0 到 1.1 版本的转换有相当小的变化。 【ODF 1.2版本】(https://www.oasis-open.org/standards#opendocumentv1.2)是ODF规范的最新版本，开发者开发ODS读/写相关的应用，请参考。

## 文件格式规范

OpenDocument 格式支持将文档表示为单个 XML 文档以及作为 [ZIP](/zh/Compression/ZIP/) 存档的包中的多个子文档的集合。 ZIP 存档中的每个文件都存储了完整文档的一部分。每个子文档存储文档的特定方面。例如，一个子文档包含样式信息，而另一个子文档包含文档的内容。典型的 ODF 文档具有以下组件：

* content.xml – 文档内容和内容中使用的自动样式。
* styles.xml – 文档内容中使用的样式和样式本身中使用的自动样式。
* meta.xml – 文档元信息，例如作者或上次保存操作的时间。
* settings.xml – 特定于应用程序的设置，例如窗口大小或打印机信息。

除此之外，包中还可以包含许多其他子文档，例如文档缩略图、图像等。文档文件是 ODF 文件的子集，其中内容（工作表）存储在 //content.xml// 子文档中。

## 参考 ＃＃

* [OpenDocument - 维基百科提供](https://en.wikipedia.org/wiki/OpenDocument)

