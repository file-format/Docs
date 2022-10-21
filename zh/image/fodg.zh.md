{
  "date" : "2019-10-11",
  "keywords" :["fodg 文件","fodg 文件格式","什么是 fodg 文件","文件","fodg 示例","fodg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument 绘图文件格式",
  "description":"了解 FODG 文件格式和可以创建和打开 FODG 文件的 API。",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .fodg 文件？

带有 .fodg 扩展名的文件是一种 Apache OpenOffice 绘图文件格式，用于存储绘图元素。它基于推进结构信息标准 (OASIS) 概述的文件格式规范。 OpenOffice 图形的另一种类似文件格式是 [ODG](/zh/image/odg/)，它将绘图元素存储为矢量图像。 FODG 文件可以使用 OpenOffice 和 LibreOffice 打开。例如，OpenOffice 支持的其他文件格式包括 [ODT](/zh/word-processing/odt/)、ODF、[ODP](/zh/presentation/odp/) 和 [ODS](/zh/spreadsheet/ods/)。

## FODG 文件格式

FODG 基于符合 OASIS OpenDocument Format ISO/IEC 26300 的 OpenDocument 的 XML 文件格式。它的 Internet 媒体类型为 application/vnd.oasis.opendocument.graphics，也符合 org.oasis-open.opendocument public.composite-content . XML 结构对于所有文档类型都是通用的，例如电子表格、绘图文件和文本文档。 OpenOffice 文档通过将内容、样式、元数据和应用程序设置分成四个单独的 XML 文件来利用关注点分离。

`<office:document-content> ` - 文档内容和内容中使用的自动样式。
`<office:document-styles> ` - 文档内容中使用的样式和样式本身中使用的自动样式。
`<office:document-meta> ` - 文档元信息，例如作者或上次保存操作的时间。
`<office:document-settings> ` - 特定于应用程序的设置，例如窗口大小或打印机信息。

## 参考 ＃＃
* [v 1.3 标准化的未来规范](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS 办公应用开放文档格式](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 格式 - 维基百科](https://en.wikipedia.org/wiki/OpenDocument)

