{
  "date" : "2019-12-10",
  "keywords" :["XLTX","文件","扩展名","文件格式","Excel Open XML","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南,了解什么是 XLTX 文件以及可以创建和打开它们的 API。",
  "title" :"什么是 XLTX 文件？",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是一 .XLTX 文件？

扩展名为 .xltx 的文件代表基于 Office OpenXML 文件格式规范的 Microsoft Excel 模板文件。它用于创建标准模板文件，可用于生成 [XLSX](/zh/spreadsheet/xlsx/) 文件，这些文件显示与 XLTX 文件中指定的相同设置。

## 历史简介

2000 年初，Microsoft 决定进行更改以适应 **Office Open XML** 的标准。在这个新标准下，不同类型的文档通过在其扩展名中附加“X"来标识，其中“X"代表 XML。到 2007 年，这种新的文件格式成为 Office 2007 的一部分，并且在新版本的 Microsoft Office 中也得到了延续。新的文件类型增加了文件大小小、损坏变化少和格式良好的图像表示的优点。

## XLTX 文件格式规范

XLTX 文件基于 Office OpenXML 文件格式并使用 XML 和 [ZIP](/zh/compression/zip/) 来减小文件大小。它是随 Microsoft Office 2007 的发布而创建的，用于替换二进制 XLT 文件格式。与 XLTX 类似，XLT 文件格式可用于使用 Microsoft Excel 2003 和 2007 创建 [XLS](/zh/spreadsheet/xls/) 文件。可以通过双击文件使用 Microsoft Excel 打开这些文件。可以通过将文件重命名为 ZIP 然后将其内容提取到光盘来观察 XLTX 文件格式的文件组织。

### [Content_Types].xml ###

这是解压缩 zip 时在基本级别找到的唯一文件。它列出了包中部件的内容类型。此 XML 文件中引用了对包中包含的 XML 文件的所有引用。

### \_rels（文件夹）###

这是包含存储包级关系的单个 XML 文件的关系文件夹。 Xltx 文件的关键部分的链接作为 URI 包含在此文件中。这些 URI 标识每个关键部分与包的关系类型。这包括与位于 xl/workbook.xml 中的主要办公文档的关系以及 docProps 中的其他部分作为核心和扩展属性。

### 文档属性 ###

此文件夹包含整个文档属性。其中包括一组核心属性、一组扩展或特定于应用程序的属性以及文档的缩略图预览。空白工作簿在此文件夹中有两个文件，即 app.xml 和 core.xml。 core.xml 包含作者、创建和保存日期以及修改日期等信息。 App.xml 包含有关文件内容的信息。

### xl（文件夹）###

这是包含有关工作簿内容的所有详细信息的主文件夹。默认情况下，它具有以下文件夹：

* \_rels
* 主题
* 工作表

和以下 xml 文件：

* 样式.xml
* 工作簿.xml

## 参考 ＃＃

* [[MS-XLSX] - .Xlsx 文件格式](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

