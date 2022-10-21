{
  "date" : "2020-08-20",
  "keywords" :["cff 文件","cff 文件格式","什么是 cff 文件","文件","cff 示例","cff 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - 紧凑字体文件格式",
  "description":"了解 CFF 文件格式和用于创建和打开 CFF 文件的 API。",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## 什么是一 .cff 文件？

带有 .cff 扩展名的文件是一种紧凑字体格式，也称为 PostScript Type 1 或 CIDFont。 CFF 作为一个容器，将多种字体一起存储在一个称为 FontSet 的单元中。 CFF 字体的设计允许嵌入 PostScript 语言代码，允许格式的额外灵活性和可扩展性以用于打印机环境。 CFF 字体文件可以使用 [Aspose.Font](https://products.aspose.com/font) 等 API 打开和转换。

## CFF 文件格式

CFF 文件是包含结构化数据布局、已定义数据类型、标题、字形组织和表字典的二进制文件。有关这些的更多详细信息，请参阅 [紧凑字体格式规范](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)。

### 数据布局
CFF 文件格式的数据布局如下图所示。

|条目|评论|
---|---|
|页眉|–|
|名称索引|-|
|顶部 DICT 指数|–|
|字符串索引|–|
|全球子指数|-|
|编码-字符集|-|
|FDSelect|仅CIDF字体|
|字符字符串索引|每个字体|
|Font DICT INDEX|每个字体，仅限 CIDFonts|
|私有 DICT|每字体|
|本地子索引|CIDFonts 的每个字体或每个私有 DICT|
|版权和商标声明|–|

### 数据类型

CFF 数据类型如下表所示。

|名称|范围|描述|
---|---|---|
|Card8|0 –255|1 字节无符号数|
|Card16|0 – 65535|2 字节无符号数|
|偏移量|可变|1、2、3 或 4 字节偏移量（由 OffSize 字段指定）|
|OffSize|1–4|1 字节无符号数指定一个或多个 Offset 字段的大小|
|SID|0 – 64999|2 字节字符串标识符|

### 标题

二进制数据以具有下表所示格式的标头开始。

|类型|名称|描述|
---|---|---|
|Card8|major|格式化主版本（从1开始）|
|Card8|次要|格式化次要版本（从 0 开始）|
|卡8|hdrSize|标头大小（字节）|
|OffSize|offSize|绝对偏移 (0) 大小|

## 参考

* [紧凑字体格式表](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF 文件格式](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 图表集](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

