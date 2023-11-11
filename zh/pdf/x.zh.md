{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/X 文件格式",
  "description":"了解 PDF/X 文件格式和可以创建和打开 PDF/X 文件的 API。",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "identifier":"pdf-zh-x"
}
},
  "lastmod" : "2019-09-10"
}

# 什么是 PDF/X 文件？ #

PDF/X 是 2001 年发布的 ISO 15930 标准，具有 PDF 功能的子集。该标准是根据印刷出版行业的具体要求制定和发布的。本标准的要求都是根据印刷出版行业的不同需求而设计的。 PDF/X 要求符合的文件是完整的，即自包含的。这要求页面中使用的字体等元素应该是文档的一部分。 3D 或视频等内容不能成为 PDF/X 文档的一部分。 PDF/X 文档中包含的信息要求其准确无误。

## PDF/X 标准和修订##

PDF/X 系列标准包含多个版本，每个版本都针对特定结果而设计。这些标准的制定旨在满足印刷和出版行业的多种不同需求。

* `PDF/X-1a` - 也被称为 PDF/X 系列的第一个标准，PDF/X-1a 要求所有内容都是 PDF 文档的一部分才能打印。不允许使用字体、表单、密码保护和可见注释等文档元素。 PDF/X-1a 有自己的特定要求，例如与透明度和图层有关的要求。这些还要求打印元素仅使用 CMYK、灰度或专色，导致不使用 RGB 或与设备无关的色彩空间。用于所有文件都以 CMYK（和/或专色）交付的交换，没有 RGB 或颜色管理数据。 PDF/X-1a 也称为完整交换，因为它要求信息的完整性
* `PDF/X-3` - 于 2002 年推出，解除了 PDF/X-1a 的许多限制。这使 PDF/X-3 中的图形能够使用基于 CMYK、grescale、RGB、Lab 和 ICC 的色彩空间。它实际上是基于带有 [ICC 配置文件](https://en.wikipedia.org/wiki/ICC_Profile) 的 PDF 标准 1.3。它也被称为颜色管理，因为它引入了与 PDF 文档中包含的颜色相关的灵活性和规则。
* `PDF/X-4` - 支持透明胶片，因此 PDF-X/4 包含输出所需的所有数据而无需展平。
* `PDF/X-5` - 基于 PDF/X-4，通过参考 XObjects 添加对外部图形的支持，以及用于渲染意图的外部 n-colorant 配置文件。使用 PDF 1.6 版进行部分打印数据交换

## 参考 ＃＃

* [PDF/X - 维基百科提供](https://en.wikipedia.org/wiki/PDF/X)

