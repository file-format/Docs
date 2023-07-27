{
  "date" : "2021-01-21",
  "keywords" :["ai文件","ai文件格式","什么是ai文件","文件","ai示例","ai文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator 图稿文件",
  "description":"了解 AI 文件格式和可以创建和打开 AI 文件的 API。",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## 什么是一 .ai 文件？

具有 .ai 扩展名的文件是 Adobe Illustrator Artwork 文件，在单个页面中包含矢量图形。它使用点来创建显示图像数据的路径，从而确保在放大时不会丢失图像质量。 AI 文件格式是类似于 AI 文件的 PGF 文件格式的基础。 AI 格式主要用于徽标和印刷媒体，其初始版本被认为类似于 [EPS](/zh/page-description-language/eps/) 文件。 AI 文件可以使用 Adobe Illustrator、Adobe Acrobat DC、PaintShop Pro 和 CorelDraw 图形工具打开。

## 人工智能文件格式

AI 是 Adobe Illustrator 的专有文件格式，并使用类似于 PGF 的双路径方法来保存与 EPS 兼容的文件。 [Adobe Illustrator 文件格式规范](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) 提供了详细的此文件格式的内部详细信息的开发人员参考。所有 Adobe Illustrator 创建的文档（文件）都是 PostScript 语言文档，有两个主要部分符合文档结构约定：“序言"和“脚本"。

### 序言

序言部分封装了解释文件所需的信息。一个例子是包含页面上所有标记的边界框。它还包含资源信息，例如字体和过程定义。这些资源在逻辑上分组到称为 procsets 的集合中，并包含用于初始化和终止其过程的显式方法。

＃＃＃ 脚本

页面上的图形元素由脚本描述。脚本包含对序言中的运算符和过程的引用，以及操作数和数据。脚本的三个逻辑部分包括：

* 设置序列 - 初始化和激活序言中定义的资源
* 描述性运算符的序列
* 停用资源的预告片

脚本中的运算符是用 prolog 中的 procset 定义的语言编写的图形元素序列。这些序列由数据元素的集合、图形属性定义和对过程集中定义的过程的调用组成。

### 对象标签

对象标签用于将自定义信息附加到 Adobe Illustrator 艺术对象。标签包括：

* 标签标识符
* 标签类型
* 数据

## 参考
* [Adobe Illustrator 文件格式规范](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [PaintShopPro 的 AI 文件格式](https://www.paintshoppro.com/en/pages/ai-file/)

