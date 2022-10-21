{
  "date" : "2019-10-11",
  "keywords" :["mht","mht 文件","mht 文件格式","mht 文件类型","文件","类型","什么是 mht 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML 文件格式",
  "description" :"了解 MHT 文件格式和用于创建和打开 MHT 文件的 API。",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## 什么是一 .mht 文件？

具有 .mht 扩展名的文件是一种启用 MIME 的归档文件格式，它在单个文件中包含不同类型的数据。它可以以 [CSS](/zh/web/css/) 文件、JavaScript 和其他资源的形式将文本、图像、页面样式等数据作为嵌入资源存储在其中。 MHT 文件，具有 MIME 类型 message/rfc822，将 HTML 文件的所有内容封装为单个存档文件，用于存储在存储设备上的存档中。 Microsoft Word 等软件应用程序可让您通过导出为 MHT 文件将 WORD 文档转换为 MHT。 MHT 文件可以使用流行的浏览器打开，例如 Microsoft Internet Explorer 和 Google Chrome。

## MHT 文件格式

与 [MHTML](/zh/web/mhtml/) 一样，MHT 也是聚合 HTML 文档的 MIME 封装。 MHT 文档中的文档内容（例如内联图片、样式表、小程序等）是 MIME-ecn 编码的，其中这些内容通过 URI 链接到根资源。 Microsoft Outlook 等电子邮件客户端以 MHT 文件格式存储电子邮件（通常为 [EML](/zh/email/eml/)）。 MHT 文件格式的完整规范可在 [RFC 822](https://tools.ietf.org/html/rfc822) 中找到，并可参考用于可处理 MHT 文件的软件应用程序开发。

## MHT和MHTML之间的区别

在保存在线页面时，要求用户确定在线页面必须保存在本机系统上的文件格式类型。最典型的情况是，用户会混淆标记语言和 MHTML 文件格式。他们注意到在这些文件格式之间看到更健康的文件格式很麻烦。

当用户决定避免浪费在线页面作为标记语言时，就会形成一个文件夹，其中包含页面不同内容的多个文件，即为文本、图形、小程序等创建的完全不同的文件区域单元。另一方面，保存在线页面作为 MHTML 为完整的在线页面创建一个文件。页面的所有元素以及嵌入在一个文件中的图形、链接和替代文件区域单元。

自然地，处理 MHT 或 MHTML 文件很简单，因为这些文件可以简单地通过电子邮件进行保护和共享。然而，标记语言文件区域单元在信息丢失的可能性之下，因为即使一个文件丢失或删除，也可能产生对用户无用的完整标记语言文件夹。

## 参考

* [MHTML - 维基百科](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

