{
  "date" : "2021-03-23",
  "keywords" :["OEBZIP","打开电子书出版结构","扩展","格式","电子书","OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 OEBZIP 文件格式和可以创建和打开 OEBZIP 文件的 API。",
  "title" :"OEBZIP - 压缩的开放式电子书出版结构",
  "linktitle" : "OEBZIP",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## 什么是 .oebzip 文件？ ##

OEBZIP 文件由国际数字出版论坛 (**IDPF**) 推出。同样，[OEB](/zh/ebook/oeb/)，这些文件是基于 XML 的电子书结构、内容和表示规范，但它是压缩或 zip 格式。

## OEBZIP 文件格式的技术细节##

OEBZIP 在呈现控制领域提供了更多新功能，其中包括改进标记词汇（现在是 XHTML 1.1 的基本子集），以及广泛扩展的 CSS 支持。与早期版本相比，可持续性因素没有变化。

OEBZIP 文件格式由一组文件组成，包括一个强制包文件，其中包括一个清单，其中列出了所有其他组件文件，以及一个表明逻辑阅读顺序的书脊。此外，对于 [XML](/zh/web/xml/) 中的文本，OEBZIP 文件的阅读器必须能够呈现 [JPEG](/zh/image/jpeg/) 和 [PNG](/zh/image/png/) 格式的图像.可以合并其他格式的内容组件，但必须以基本 OEB 格式之一提供后备内容。
  

OEBZIP 文件包主要用作中间状态格式，通过出版商或聚合商管理向最终用户发布，这些出版商或聚合商以适合不同电子书查看者的形式提供电子书。其后续版本 [EPUB](/zh/ebook/epub/) 更有可能以最终状态格式和中间状态格式接触最终用户。

## 参考

* [OEBPS（开放电子书论坛出版结构）1.2]（https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml）
* [打开电子书](https://en.wikipedia.org/wiki/Open_eBook)


