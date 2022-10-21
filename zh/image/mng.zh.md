{
  "date" : "2019-10-11",
  "keywords" :["mng 文件","mng 文件格式","什么是 mng 文件","文件","mng 示例","mng 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG 文件格式 - 多图像网络图形文件格式",
  "description":"了解 MNG 文件格式和可以创建和打开 MNG 文件的 API。",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .mng 文件？

扩展名为 .mng 的文件是一种多图像网络图形文件格式，类似于 [PNG](/zh/image/png/) 图像格式，但支持动画图像。它的开发是为了避免使用动画的附加功能使 PNG 格式过载。 MNG 也类似于 [GIF](/zh/image/gif/) 文件，但使用更多压缩并支持完整的 alpha 功能。 MNG 文件的非官方 MIME 媒体类型是 video/x-mng。 MNG 文件可以在 ImageMagik 和 IrfanView 等应用程序中打开。

## MNG 文件格式

MNG 文件格式与 PNG 类似，并使用与 PNG 规范中定义的相同的块结构。 MNG 解码器必须能够解码 PNG 数据流，而无需为解码指令指定任何特殊标志。 MNG 将多个图像组合成一个“帧"，其中一些图像用作从一个位置移动到另一个位置的精灵。该机制允许重用图像数据而不重新传输它。 [MNG 规范](http://www.libpng.org/pub/mng/spec/) 可供开发者参考。

### MNG 签名

MNG 数据流以 8 字节签名开始，其中包含：

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

这类似于 PNG 签名，但包含 MNG 而不是 PNG。

### MNG 帧

MNG 帧由较小图像的二维图像组成。可以使用行和列索引组合访问每个小图像。该格式能够存储排列成一系列二维平面的三维“体素"数据。每个平面由 PNG 或 Delta-PNG 数据流表示。每个 Delta-PNG 数据流将图像定义为与父 PNG 图像的差异。与为每个图像使用完整的 PNG 数据流相比，这提供了一种更紧凑的方式来表示后续图像。

## 参考 ＃＃

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG 格式 v 1.0](http://www.libpng.org/pub/mng/spec/)

