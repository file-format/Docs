{
  "date" : "2019-10-11",
  "keywords" :["XPS","XML 纸张规格","文件","扩展名","文件格式","EMF","PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - 页面布局文件格式",
  "description":"了解 XPS 文件格式和可以创建和打开 XPS 文件的 API。",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## 什么是一 .xps 文件？ ##

XPS 文件表示基于 Microsoft 创建的 XML 纸张规范的页面布局文件。它是作为 EMF 文件格式的替代品而开发的，类似于 [PDF](/zh/pdf/) 文件格式，但在文档的布局、外观和打印信息中使用 XML。事实上，更合理的说法是 XPS 是对 PDF 的尝试，但由于多种原因未能获得 PDF 所拥有的足够普及。 Microsoft 从 Windows 7 开始默认提供 XPS Document Writer 用于创建 XPS 文件。 XPS 文件可以通过在打印文档时选择“Microsoft XPS Document Writer"作为打印机来生成。

XPS 查看器作为 Windows Vista、Windows 7、Windows 8 和 Internet Explorer 6 或更高版本的一部分集成。 XPS 文件在生成后变为只读。这增加了用户对作为 XPS 发送的文档真实性的信心。 XPS 文档可以包含一个或多个从原始文档转换而来的页面。

## 历史简介 ＃＃

Microsoft 向 Ecma International 提交了 XPS 规范。 2007 年 6 月，Ecma 第 46 技术委员会 (TC46) 成立，以制定基于 OpenXPS 论文规范的标准。 Ecma International 于 2009 年 6 月在第 97 届大会上批准了 Ecma 标准 (ECMA-388) [XPS 规范](http://www.ecma-international.org/publications/standards/Ecma-388.htm)。

## XPS 文件格式##

XPS 格式由定义文档组成和每个页面的视觉外观的 XML 标记以及用于显示或打印文档的呈现规则组成。它保留所有信息以在任何系统上重新创建文档，使其独立于该系统上可用的资源。该格式本质上是一个 ZIP 存档，如果您将文件扩展名重命名为 ZIP，您将看到包含文档数据的组成文件。这些文件包括：

* 文档页面文件 (.fpage) - 包含文档内容和文档格式设置。 XPS 文档中的每一页都有一个 FPAGE 文件。
* 文档设置文件 (.fdoc) - 存储 XPS 存档中包含的设置。
* 文档片段文件 (.frag) - 定义实际 XPS 文件的设置，并且文档中的每个页面都有自己的 .frag 文件。

{{< figure src="../XPS-1.png" alt="XPS 文件格式" >}}

这些文件以这样一种方式保留文档内容，例如，如果某人的机器上没有安装相同的字体，XPS 查看器仍将呈现这些原始字体。这意味着每个都包含 XML 标记文件：

* 页
* 文本
* 嵌入字体
*光栅图像
* 2D矢量图形
* 数字版权管理

XPS 文档格式包括一组明确定义的部分和关系，每个部分和关系都实现了文档中的特定目的。该格式还扩展了包功能，包括数字签名、缩略图和交错。

典型的 XPS 文档如下所示，可以根据 XPS 文件格式 [规范](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf) 进行分析。

{{< figure src="../XPS-2.png" alt="XPS 文件格式" >}}


## 参考 ＃＃

* [XPS 文件格式规范](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS - 维基百科提供](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

