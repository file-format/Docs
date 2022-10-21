{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南,了解什么是 _XLSX 文件以及可以创建和打开 _XLSX 文件的 API。",
  "title" :"什么是 _XLSX 文件？",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## 什么是 _XLSX 文件？

带有 .\_xlsx 扩展名的文件实际上是一个 [XLSX](/zh/spreadsheet/xlsx/) 文件，它被其他应用程序重命名。当文件名包含 .在文件名的末尾。 \_XLSX 文件可以在 Microsoft Excel 中打开，类似于 XLSX 文件，方法是再次将它们重命名为 .xlsx 扩展名。

## _XLSX 文件格式 - 更多信息

_XLSX 文件与 XLSX 文件没有什么不同，并使用 Microsoft 早在 2000 年采用的 Open XML 标准。在 XLSX 之前，[XLS](/zh/spreadsheet/xls/) 是用于处理 Excel 电子表格以保存文档的主要文件格式以二进制格式。这种新的基于 XML 的文件格式具有文件大小小、防止文件损坏和格式良好的图像表示等优点。这种新的基于 XML 的文件格式成为 Office 2007 的一部分，并且也在新版本的 Microsoft 中执行。

## \_XLSX 文件格式规范

由于 \_XLSX 文件是重命名的 XLSX 文件，因此它与原始文件具有相同的规格。它只是一个基于 [ZIP](/zh/compression/zip/) 存档文件格式的存档文件。如果要查看此存档的内容，只需将文件重命名为 .zip 扩展名并将其解压缩即可查看此 Excel 工作簿的组成文件。空白工作簿在提取到其文件时具有以下组成文件和文件夹。

### [Content_Types].xml

这是解压缩 zip 时在基本级别找到的唯一文件。它列出了包中部件的内容类型。此 XML 文件中引用了对包中包含的 XML 文件的所有引用。

### \_rels（文件夹）

这是包含存储包级关系的单个 XML 文件的关系文件夹。 Xlsx 文件的关键部分的链接作为 URI 包含在此文件中。这些 URI 标识每个关键部分与包的关系类型。这包括与位于 xl/workbook.xml 中的主要办公文档的关系以及 docProps 中的其他部分作为核心和扩展属性。

### 文档属性

此文件夹包含整个文档属性。其中包括一组核心属性、一组扩展或特定于应用程序的属性以及文档的缩略图预览。空白工作簿在此文件夹中有两个文件，即 app.xml 和 core.xml。 core.xml 包含作者、创建和保存日期以及修改日期等信息。 App.xml 包含有关文件内容的信息。

### xl（文件夹）

这是包含有关工作簿内容的所有详细信息的主文件夹。默认情况下，它具有以下文件夹：

* \_rels
* 主题
* 工作表

和以下 xml 文件：

* 样式.xml
* 工作簿.xml

## 参考

* [MS-XLSX - .xlsx 文件格式](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

