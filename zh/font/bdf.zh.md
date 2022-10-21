{
  "date" : "2021-02-25",
  "keywords" :["bdf 文件","bdf 文件格式","什么是 bdf 文件","文件","bdf 示例","bdf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - 字形位图分布格式",
  "description":"了解 BDF 文件格式和可以创建和打开 BDF 文件的 API。",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## 什么是一 .bdf 文件？
BDF 文件是人类可读的形式，通常以 ASCII 编码分发。该文件以与完整字体相关的全局信息开头，然后是各个字形的信息和位图。其中的数据显示了单一尺寸方向的字体。用于多个方向的度量可以包含在单个文件中。在 BDF 文件中，每个项目都包含在文件中单独的文本行中。空格用于分隔一行中的项目。

## BDF 文件格式
字形位图分布格式的 BDF 缩写； Adobe 拥有的一种文件格式，用于保存位图类型的字体。内容采用文本文件的形式，旨在供计算机和人类阅读。 BDF 特别用于 Unix X Window 环境。它已被应该更有效的 PCF 字体格式以及 OpenType 和 TrueType 字体广泛取代。
### BDF文件结构
BDF 字体文件由三个部分组成：

- 适用于字体中所有字形的全局部分。
- 每个字形都有一个单独的条目的部分。
- ENDFONT 语句。

## 例子
这是一个包含一个字形的示例字体，用于 ASCII 大写“A"。它的全局声明以“STARTFONT"行开始，以“CHARS"行结束
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## 参考
* [字形位图分布格式](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [字形位图分布格式（BDF）规范]（https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf）

