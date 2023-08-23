{
  "date" : "2019-10-11",
  "keywords" :["wmz 文件","wmz 文件格式","什么是 wmz 文件","文件","wmz 示例","wmz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ 文件格式 - 压缩的 Windows 元文件",
  "description":"了解 WMZ 文件格式和可以创建和打开 WMZ 文件的 API。",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## 什么是一 .wmz 文件？

扩展名为 .wmz 的文件是 [WMF](/zh/image/wmf/) 的压缩版本，用于存储元文件。它是由旧版本的 Microsoft Office 应用程序生成的中级文件，不是很常用。 WMZ 文件是在将文档保存为 [HTML](/zh/web/html/) 格式时生成的。这些也可能在通过电子邮件发送包含嵌入式剪贴画、方程式等的文档时生成。可以打开 WMZ 文件的应用程序包括（但不限于）Corel Winzip 和 Apple Archive Utility。

## WMZ 文件格式

WMZ 文件经过 [Gzip](/zh/compression/gz/) 压缩，内部包含 [WMF](/zh/image/wmf/)。 Gzip 使用 DEFLATE 算法来压缩存档。 GZIP 不同于 [ZIP](/zh/compression/zip/) 存档格式，因为它应用压缩算法来完成存档而不是单个文件。文件格式包括：

* 文件头
* 可选标题
* 压缩数据
* 文件页脚

由 Internet 工程任务组 (IETF) 发布的 GZIP 文件格式 [规范版本 4.3](https://datatracker.ietf.org/doc/html/rfc1952) 包含有关文件格式的详细信息。

## 参考

* [RFC1952：GZIP 文件格式规范](https://datatracker.ietf.org/doc/html/rfc1952)，由 [IETF](https://www.ietf.org)
* [Windows 元文件 - 维基百科](https://en.wikipedia.org/wiki/Windows_Metafile)

