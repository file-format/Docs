{
  "date" : "2019-10-11",
  "keywords" :[ "apng 文件", "apng 文件格式", "什么是 apng 文件", "文件", "apng 示例", "apng 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG 文件格式 - 动画便携式网络图形文件",
  "description":"了解 APNG 文件格式和可以创建和打开 APNG 文件的 API。",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是 .APNG 文件？

带有 .apng（动画便携式网络图形）扩展名的文件是一种光栅图形格式，是便携式网络图形 ([PNG](/zh/image/png/) ) 的非官方扩展名。它由表示动画序列的多个帧（每个 PNG 图像）组成。这提供了与 [GIF](/zh/image/gif/) 文件类似的可视化效果。 APNG 文件支持 24 位图像和 8 位透明度。 APNG 向后兼容非动画 GIF 文件。 APNG 文件使用相同的 .png 扩展名，可以由 Mozilla Firefox、支持 APNG 的 Chrome、iOS 10 的 iMessage 应用程序等应用程序打开。

## 历史简介

* APNG 规范创建于 2004 年，以提供对动画 PNG 图像的支持
* APNG 解码器的开发尺寸要小得多，并使用 PNG 解码器的背面
* 经过不断的思考，制定了一个新的MIME类型image/apng，同时保持扩展名与.png相同而不是.apng
* APNG 于 2007 年 4 月 20 日被 PNG 组正式拒绝，原因是它对 PNG 图像的统一性，同时具有不同的规格

## APNG 文件格式

APNG 文件以二进制文件的形式存储在磁盘上，并使用 PNG 的扩展规范来处理动画图像。 APNG 文件的第一帧是一个普通的 PNG 流，PNG 解码器可以读取以进行显示。 APNG 文件格式遵循 PNG 规范，数据存储在称为块的段中。但是，APNG 引入了以下新块：

`Animation Control Chunk (acTL)` - 表示此文件是动画 PNG 文件，而不是普通的 PNG 文件。它充当标记，位于 IDAT 块之前。它还包含帧数和有关循环动画时间的信息

`Frame Control Chunk` - 出现在每个元数据信息的开头，例如尺寸、位置、透明度应用程序，以及一旦结束后上一帧或下一帧的替换信息。

`Frame Data Chunk` - 存储帧的内容并以序列号开始。此序列号与默认图像的 IDAT 块具有相同的结构。

{{< figure src="../APNG.png" alt="动画 PNG - APNG 文件格式" >}}

APNG 与 PNG 向后兼容，因为横向规范的设计方式是，读取 PNG 文件的应用程序应该简单地忽略它不理解的块。关于位深度、颜色类型、压缩、过滤器、隔行扫描方法和调色板信息的规范使用与默认 PNG 格式相同的规范。

## APNG 与 GIF

由于 GIF 已经到位并被长期使用，您可能想知道 APNG 与 GIF 有何不同。以下是 APNG 和 GIF 之间的一组比较，简要介绍了这两种文件格式。

||APNG|GIF|
---|---|---|
|出版|2004|1987|
|色深|24 位|8 位|
|帧率|无限制|每秒 10 帧|
|透明度|完全和部分|完全|
|压缩|很好|好|

## 参考

* [APNG 文件格式](https://en.wikipedia.org/wiki/APNG)
* [官方PNG格式规范](https://www.w3.org/TR/PNG/)

