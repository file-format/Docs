{
  "date" : "2020-08-20",
  "keywords" :["otf 文件","otf 文件格式","什么是 otf 文件","文件","otf 示例","otf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType 字体文件格式",
  "description":"了解 OTF 文件格式和可以创建和打开 OTF 文件的 API。",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## 什么是一 .otf 文件？

带有 .otf 扩展名的文件是指 OpenType 字体格式。 OTF 字体格式更具可扩展性，并扩展了数字排版的 [TTF](/zh/font/ttf/) 格式的现有功能。 OTF 由 Microsoft 和 Adobe 开发，结合了 PostScript 和 TrueType 字体格式的功能。这使得 OTF 格式可以适应大多数书写系统，这就是它在主要计算机平台上统一使用的原因。 Mac OS X 和 Windows 2000 及更高版本支持 OpenType 字体格式。

## 历史简介

对 OpenType 字体的需求源于对能够处理精细排版的更具表现力的字体格式的需求。此外，它旨在满足世界上许多书写系统复杂行为的要求。微软在 1990 年代初尝试授权 Apple 的高级排版技术，即 GX Typography。这并不顺利，因此，微软在 1994 年开始增强其自己的 TrueType 字体技术。修改还包括引入更合适的字体格式，该格式也符合 Adobe 的 Type 1 (PostScript) 字体格式的功能。

Adobe 于 1996 年加入微软，努力取代 Apple 的 TrueType 和它自己的 Type 1 字体格式。这导致了两种底层字体格式的组合，以克服限制并添加新的扩展。这项新技术于同年推出，名称为 **OpenType**。

## OTF 文件格式规范

OTF 规范由 Microsoft 公开提供，可以从开发人员的角度参考。与 TTF 一样，它使用相同的 'sfnt' 容器结构并与 TrueType 规范兼容。 OpenType 字体文件中的数据用于不同目的，例如计算文本布局、将字形定义为 TrueType 或紧凑字体格式 (CFF) 轮廓、提供单色或彩色位图或 SVG 文档作为替代字形描述以及元数据信息。

### OTF 数据类型
OTF 文件使用以下数据类型，这些数据类型均采用 Big Endian。

|数据类型|说明|
---|---|
|uint8| 8 位无符号整数。|
|int8| 8 位有符号整数。|
|uint16| 16 位无符号整数。|
|int16| 16 位有符号整数。|
|uint24| 24 位无符号整数。|
|uint32| 32 位无符号整数。|
|int32| 32 位有符号整数。|
|固定| 32 位有符号定点数 (16.16)|
|FWORD| int16 描述字体设计单位中的数量。
|UFWORD| uint16 描述字体设计单位中的数量。
|F2DOT14| 16 位有符号固定数，小数的低 14 位 (2.14)。|
|长日期时间|日期和时间以 UTC 1904 年 1 月 1 日午夜 12:00 后的秒数表示。该值表示为带符号的 64 位整数。
|标签|四个 uint8 数组（长度 = 32 位），用于标识表格、设计变化轴、脚本、语言系统、功能或基线|
|偏移16|表的短偏移量，与 uint16 相同，NULL 偏移量 = 0x0000|
|偏移32|表的长偏移量，与 uint32 相同，NULL 偏移量 = 0x00000000|
|Version16Dot16|包含主要和次要版本号的 32 位值。 （见表版本号。）|

### OTF 表目录

OTF 文件以表目录开头。该目录是字体文件中表的顶级集合。根据文件中字体的数量，表目录可能位于文件中的不同位置。例如，如果字体文件只有一种字体，则表目录从文件的字节 0 开始。如果有多个 OpenType 字体集合，
表目录开头在 TTCHeader 中指示。

|类型 |名称 |描述|
---|---|---|
|uint32 |sfnt版本| 0x00010000 或 0x4F54544F ('OTTO')|
|uint16| numTables |表的数量。|
|uint16| searchRange |小于等于 numTables 的 2 的最大幂乘以 16 ((2\**floor(log2(numTables))) * 16，其中“**"是取幂运算符)。|
|uint16 |entrySelector log2 的最大幂 2 小于等于 numTables (log2(searchRange/16)，等于 floor(log2(numTables)))。|
|uint16 |rangeShift |numTables 乘以 16，减去 searchRange ((numTables * 16) - searchRange)。|
|表格记录| tableRecords[numTables] |表记录数组—字体中的每个顶级表都有一个|


### 表记录

对于字体中的每个顶级表，都有一个由以下字段组成的表记录。

|类型|姓名|说明|
---|---|---|
|标签|表标签|表标识符。|
|uint32|校验和|此表的校验和。|
|偏移32|偏移|字体文件开头的偏移量。|
|uint32| length 此表的长度。|

OpenType 字体文件中的每个表格都由称为表格标签的名称表示。数组中的所有记录必须按标签升序排序。

## 参考
* [Microsoft 的 OpenType 字体规范](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType 概述](https://learn.microsoft.com/en-us/typography/truetype/)

