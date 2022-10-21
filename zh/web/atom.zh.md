{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ATOM 文件 - Atom 联合格式",
  "description" :"了解什么是 ATOM 文件以及可以创建和打开 ATOM 文件的 API。",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## 什么是 .ATOM 文件？

ATOM 文件是一种用于 Atom 提要和条目文档结构的联合格式。与 .RSS 文件类似，ATOM 文件格式是一种基于 XML 的联合格式，是发布内容的标准。 ATOM 文件用于网络提要，允许软件程序检查网站上发布的更新。它包含不同类型的条目，例如标题、全文文章、摘录或网站内容的链接

可以**打开 ATOM 文件**的应用程序包括 **Apple Safari**。

## ATOM 文件格式 - 更多信息

ATOM 文件以流行的 XML 文件格式存储和发布，这是一种用于信息交换的通用格式。考虑到 RSS 文件格式的局限性和缺陷，它是作为 RSS 的替代品而开发的。

### Atom 文档的类型

1. `Atom Entry Documents` - 它是一个 XML 文档，由 Atom 提要的单个信息项（称为条目）组成。它有一个<atom:entry>包含许多子元素的元素。 Atom 条目的内容可以是纯文本、HTML、XHTML 或其他 IANA（互联网号码分配机构）媒体类型。
1. `Atom Feed Documents` - 它是一种 XML 文档，提供有关 Atom 提要的元数据以及提要的一个或多个条目。当客户端从提要中请求信息时，提要文档由服务器生成，其中包括许多用于满足请求的 Atom 条目。
1. `Atom Collection` - 它是一种特殊的 Atom 提要文档，包含可编辑的 Atom 条目的 URL。

## 参考

* [Atom 联合格式 - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Atom 提要概述 - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - 网络标准](https://en.wikipedia.org/wiki/Atom_(web_standard))

