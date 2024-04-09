{
  "date" : "2019-10-11",
  "keywords" :["xml","文件","扩展名","文件格式","文件扩展名","可扩展标记语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML 文件格式",
  "description":"了解 XML 文件格式和可以创建和打开 XML 文件的 API。",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 XML 文件？

XML 代表可扩展标记语言，类似于 **[HTML](/zh/web/html/)** 但在使用标签定义对象方面不同。创建 XML 文件格式背后的整个想法是在不依赖软件或硬件工具的情况下存储和传输数据。它的流行是因为它既是人类可读的又是机器可读的。这使其能够以对象的形式创建通用数据协议，以便通过网络（如万维网 (WWW)）存储和共享。 XML 中的“X"表示可扩展，这意味着该语言可以根据用户要求扩展到任意数量的符号。正是因为这些特性，许多标准文件格式都使用了它，例如 Microsoft Open XML、LibreOffice OpenDocument、**[XHTML](/zh/web/xhtml/)** 和 **[SVG](/zh/page-description-language/svg/)**。

## XML 文件格式

XML 文件格式基于 XML 文档对象模型 (DOM)，它是 HTML 和 XML 文档的编程 API。 XML DOM 定义了访问和操作 XML 文档元素的标准方法。它创建 XML 文档的树结构视图，可用于通过 DOM 树访问所有元素。可以修改/删除现有元素，也可以在 XML 树中创建新元素。 XML 文档的每个元素称为一个节点。 XML DOM 如下图所示。

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### XML 的通用方法

通过简化数据传输和平台更改，XML 的强大功能使其成为网络上数据通信的通用语言。这也可以通过以纯文本格式存储数据来确保在不兼容的系统之间交换数据成为可能。 HTML 用于网络上的数据表示，而 XML 用于数据交换。 XML 中使用的标记标记对定义了阅读应用程序要使用的结构的关键元素。

## XML 示例

以下是 CD 目录的简化示例，其中每条记录都包含有关 CD 的信息，例如艺术家、国家、公司、价格和制作年份。

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## 参考

* [XML - 维基百科](https://en.wikipedia.org/wiki/XML)

