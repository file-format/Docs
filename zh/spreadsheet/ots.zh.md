{
  "date" : "2019-12-16",
  "keywords" :["OTS","文件","扩展名","文件格式","Excel","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 OTS 文件格式和可以创建和打开 OTS 文件的 API。",
  "title" :"OTS - OpenDocument 电子表格模板文件格式",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## 什么是一 .ots 文件？

扩展名为 .ots 的文件是使用 Apache OpenOffice 中包含的 Calc 应用程序软件创建的 OpenDocument 电子表格模板文件。 Calc 应用软件类似于 Microsoft Office 中的 Excel。 OTS 文件格式用于创建包含与样式、字体、数据、电子表格布局和格式相关的预定义设置的模板。 OTF 文件具有 `mime-type application/vnd.oasis.opendocument.spreadsheet-template`。这些模板文件可用作生成和保存以 [ODS 文件格式](/zh/spreadsheet/ods/) 保存的实际数据文件的起点。 OTS 文件可用于 OpenOffice 和 LibreOffice 等应用程序。

## OTS 文件格式

OTS 文件以 OASIS 的基于 XML 的 OpenDocument 文件格式保存，该格式由多个子文档的集合组成，并以 [ZIP](/zh/compression/zip/) 存档形式打包。每个 zip 存档存储完整文档的一部分，每个子文档存储文档的特定方面。例如，一个子文档包含样式信息，而另一个子文档包含文档的内容。典型的 ODF 文档具有以下组件：

### OTS 内容.xml

content.xml 文件包含文档的实际内容。但是，这不包括图像等二进制数据。
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS 文件格式的 Styles.xml

styles.xml 文件包含样式信息，并大量用于格式化和布局。样式类型包括：

* 段落样式
* 页面样式
* 字符样式
* 框架样式
* 列出样式

### 元.xml

meta.xml 文件包含有关文件元数据的信息，例如作者、上次修改日期等。
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### 设置.xml

`settings.xml` 文件包括文档级别设置，例如缩放系数和光标位置。

## 参考 ＃＃

* [OpenDocument 1.2 规范](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - 维基百科](https://en.wikipedia.org/wiki/OpenDocument)

