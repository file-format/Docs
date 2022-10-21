{
  "date" : "2021-02-26",
  "keywords" :["type1 文件","type1 文件格式","什么是 type1 文件","file","type1 示例","type1 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Type 1 - PostScript Type 1 字体",
  "description":"Type 1 字体是一种已弃用的 Adobe 产品，广泛用于可以使用 PostScript 的桌面出版软件和打印机",
  "linktitle" : "TYPE1",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-26"
}

## 什么是 Type 1 字体？

Type 1 字体是一种已弃用的 Adobe 技术，广泛用于基于桌面的发布软件和可以使用 PostScript 的打印机。尽管许多现代平台、Web 浏览器和移动操作系统不支持 Type 1 字体，但某些操作系统仍然支持这些字体。 Type 1 字体中 Unicode 信息支持的不足也限制了它们支持扩展语言字符集的能力。

## 历史简介

Type 1 字体技术于 1984 年推出，用于 Adobe 的 PostScript 页面描述语言。在 90 年代中期，Adobe 决定专注于使用更灵活的 OpenType 字体而不是 Type 1。

### Type 1 的支持何时结束？
从 2023 年 1 月开始，用户将无法再使用 Type 1 字体编写内容。在此之前，不会进行任何更改。
一些产品，如 Document Cloud 应用程序，将继续使用它们一直以来的 Type 1 字体。


## Type 1 字体的限制

类型 1 的一些已知限制如下所示：

- 它不允许在一个字体中包含超过 256 个字形。 CID 字体可以做到这一点，许多输出设备可能无法正确处理 CID 字体。
- Type 1 字体不是跨平台的。将一种平台字体转换为其他字体时需要进行复杂的转换。
- 字体名称坚持旧 DOS 时代的 8 个字符限制，这使得难以确定文件中存储的字体。

## Windows机器上的Type 1字体
Type 1 字体数据由 windows 中的两个独立文件组成：

1. 扩展名为“.PFB"的文件由大纲数据组成。
2. 扩展名为“.PFM"的文件包含度量数据。

## 参考
* [Type 1 字体](https://www.prepressure.com/fonts/basics/type1)
* [PostScript Type 1 字体支持结束](https://helpx.adobe.com/fonts/kb/postscript-type-1-fonts-end-of-support.html)
* [PostScript 字体（维基百科）]（https://en.wikipedia.org/wiki/PostScript_fonts）

