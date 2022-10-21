{
  "date" : "2019-12-10",
  "keywords" :["XLSX","文件","扩展名","文件格式","Excel","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解什么是 XLSX 文件以及可以创建和打开 XLSX 文件的 API。",
  "title" :"XLSX 文件格式 - 什么是 XLSX 文件？",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是一 .XLSX 文件？

**XLSX** 是 Microsoft 在 Microsoft Office 2007 发布时引入的 Microsoft Excel 文档的知名格式。基于根据 [第 2 部分] 中概述的开放打包约定组织的结构（https://www .ecma-international.org/publications/standards/Ecma-376.htm) 的 OOXML 标准 ECMA-376，新格式是一个包含许多 XML 文件的 zip 包。只需解压缩 .xlsx 文件即可检查底层结构和文件。

## XLSX 文件格式简史

XLSX 文件格式于 2007 年推出，使用 Microsoft 早在 2000 年采用的 Open XML 标准。在 XLSX 之前，使用的常用文件格式是 [XLS](/zh/spreadsheet/xls/)，它是纯二进制文件格式。新文件类型增加了文件大小小、损坏变化少和格式良好的图像表示的优点。 2000 年初，Microsoft 决定进行更改以适应 **Office Open XML** 的标准。到 2007 年，这种新的文件格式成为 Office 2007 的一部分，并且在新版本的 Microsoft Office 中也得到了延续。

## XLSX 文件格式规范

官方的 [XLSX 文件格式规范](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) 可从 Microsoft 在线获得。为了查看 XLSX 文件中的内容，只需通过更改其扩展名将其重命名为 [ZIP](/zh/compression/zip/) 文件，然后将其解压缩以查看此 Excel 工作簿的组成文件。空白工作簿在提取到其文件时具有以下组成文件和文件夹。

### [Content_Types].xml ###

这是解压缩 zip 时在基本级别找到的唯一文件。它列出了包中部件的内容类型。此 XML 文件中引用了对包中包含的 XML 文件的所有引用。

### \_rels（文件夹）###

这是包含存储包级关系的单个 XML 文件的关系文件夹。 Xlsx 文件的关键部分的链接作为 URI 包含在此文件中。这些 URI 标识每个关键部分与包的关系类型。这包括与位于 xl/workbook.xml 中的主要办公文档的关系以及 docProps 中的其他部分作为核心和扩展属性。

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

## XLSX 格式示例 ##


对于工作簿中包含的每个 Excel 工作表，都有一个 XML 文件。您可以在 xl/worksheets 文件夹中找到这些 XML 文件。工作表中包含的所有信息都组织在 XML 文件的不同部分中。让我们检查下图中显示的工作簿中的示例工作表。

{{< figure src="../XLSX file format.png" alt="XLSX 文件格式" >}}

可以看出，此工作表包含单元格 A1 到 B2 中的内容和图像。此外，单元格 G13 当前是工作表中的活动单元格。现在，让我们检查 xl/worksheets/sheet1.xml 文件，看看这些信息在 XML 文件中是如何表示的。该 XML 文件的内容如下所示。

{{< figure src="../XLSX File Format Details.png" alt="XPS 文件格式" >}}

1. 选项卡应用了主题颜色。它在带有标签的 XML 文件中提到<tabColor>跟随主题ID。
1. tabSelected 值设置为 1 表示这是选中的工作表
1. 如上图所示，工作表中的单元格 G13 是活动单元格，在 XML 文件中也有提及。
1. sheetData 选项卡代表工作表中包含的数据。但是，您可以看到工作表的原始内容不在此部分中。这是因为文本是从“sharedStrings"XML 表间接引用的。这种链接确保每个文本只保存一次，并且可以再次引用以节省空间。
1. 可以看到的图像由引用 id "rId2" 引用

## 贡献

必须分享有关 XLSX 或电子表格文件格式的信息？您可以在 [电子表格文件格式新闻](https://news.fileformat.com/t/Spreadsheet) 部分发布您的发现。

## 参考

* [[MS-XLSX] - XLSX 文件格式](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

