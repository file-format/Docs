{
  "date" : "2019-12-10",
  "keywords" :["XLTM","文件","扩展名","文件格式","Excel Open XML 宏","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南了解什么是 XLTM 文件以及可以创建和打开它们的 API。",
  "title" :"什么是 XLTM 文件？",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是一 .XLTM 文件？

XLTM 文件扩展名将 Microsoft Excel 生成的文件表示为启用宏的模板文件。 XLTM 文件在结构上类似于 [XLTX](/zh/spreadsheet/xltx/)，只是后者不支持使用宏创建模板文件。此类模板文件用于生成和设置布局、格式和其他设置以及宏，以便随后创建类似的 XLSX 文件。

## 历史简介 ＃＃

2000 年初，Microsoft 决定进行更改以适应 **Office Open XML** 的标准。在这个新标准下，不同类型的文档通过在其扩展名中附加“X"来标识，其中“X"代表 XML。到 2007 年，这种新的文件格式成为 Office 2007 的一部分，并且在新版本的 Microsoft Office 中也得到了延续。新的文件类型增加了文件大小小、损坏变化少和格式良好的图像表示的优点。

## XLTM 文件格式规范 ##

XLTM 文件基于 Office OpenXML 文件格式并使用 XML 和 [ZIP](/zh/compression/zip/) 来减小文件大小。这些可以通过双击文件使用 Microsoft Excel 打开。通过将文件重命名为 ZIP，然后将其内容解压缩到光盘，可以观察 XLTM 文件格式的文件组织。

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

* [MS-XLSX 文件格式](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

