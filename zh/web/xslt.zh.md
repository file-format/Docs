{
  "date" : "2021-01-20",
  "keywords" :["xslt","文件","扩展名","文件格式","文件扩展名","可扩展样式表语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT 文件格式",
  "description":"了解 XSLT 文件格式和可以创建和打开 XSLT 文件的 API。",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## 什么是 XSLT 文件？

具有 .xslt 扩展名的文件是可扩展样式表语言转换文件，用于使用 XSL 指令转换和设置 XML 文件的样式。该格式用于将 XML 文档转换为标准输出格式，例如文本文档或 .html 网页。此转换基于现有 XML 文档的内容创建一个新文档。 XSLT 使其在理论上能够进行任意计算。

## XSLT 文件格式

XLST 文件格式包含纯文本格式的转换指令，可以在任何文本编辑器中查看。该语言已进行了三次修订。

* `XSLT 1.0` - XSLT 1.0 于 1999 年 11 月作为 W3C 推荐标准发布。
* `XSLT 2.0` - 它包括修改，例如使用正则表达式的字符串操作、用于操作日期、时间和持续时间的函数和运算符、多个输出文档、分组以及更丰富的类型系统和强大的类型检查。
* `XSLT 3.0` - 它于 2017 年 6 月 8 日成为 W3C 建议的一部分，主要的新功能包括流转换、改进大型样式表模块化的包、改进的动态错误处理，例如 xsl:try 指令，并支持映射和数组，使 XSLT 能够处理 JSON 和 XML。

### XSLT 示例

以下示例取自 [w3schools](https://www.w3schools.com/xml/xsl_intro.asp)。
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## 参考 ＃＃

* [XSLT - 来自维基百科](https://en.wikipedia.org/wiki/XSLT)
* [XSLT 元素](https://en.wikipedia.org/wiki/XSLT_elements)

