{
  "date" : "2021-03-23",
  "keywords" :["OEB","开放电子书出版结构","扩展","格式","电子书","OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 OEB 文件格式和可以创建和打开 OEB 文件的 API。",
  "title" :"OEB - 开放电子书出版结构",
  "linktitle" : "OEB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## 什么是一 .oeb 文件？

OEB 文件由国际数字出版论坛 (**IDPF**) 介绍。更正式地说，OEB 文件也称为 **OEBPS**。这些文件是基于 XML 的电子书结构、内容和表示规范。此文件格式已被 [EPUB](/zh/ebook/epub/) 格式取代。

## OEB 文件格式的技术细节

OEB 文件格式由一组文件组成，包括一个强制包文件，其中包括一个列出所有其他组件文件的清单，以及一个指示逻辑阅读顺序的书脊。此外，对于 [XML](/zh/web/xml/) 中的文本，OEB 文件的阅读器必须能够以 [JPEG](/zh/image/jpeg/) 和 [PNG](/zh/image/png/) 格式呈现图像.可以合并其他格式的内容组件，但必须以基本 OEB 格式之一提供后备内容。

OEBPS 1.2 是对先前版本 (OEBPS 1.0.1) 的紧密耦合更新。它在呈现控制领域提供了现代功能，其中包括增强标记词汇（现在是 XHTML 1.1 的真正子集），并大大扩展了 CSS 支持。与早期版本相比，可持续性因素没有变化。
  

OEB 文件包主要用作中间状态格式，通过出版商或聚合商管理向最终用户发布，这些出版商或聚合商以适合不同电子书查看者的形式提供电子书。其后续版本 [EPUB](/zh/ebook/epub/) 更有可能作为最终状态格式和中间状态格式到达最终用户。

## 参考

* [OEBPS（开放电子书论坛出版结构）1.2]（https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml）
* [打开电子书](https://en.wikipedia.org/wiki/Open_eBook)


