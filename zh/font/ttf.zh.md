{
  "date" : "2020-08-20",
  "keywords" :["ttf 文件","ttf 文件格式","什么是 ttf 文件","文件","ttf 示例","ttf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType 字体文件格式",
  "description":"TrueType 字体 (TTF) 基于最初由 Apple, Inc. 设计的数字字体技术规范。Apple 和 Microsoft 在 Mac 和 Windows 操作系统上都使用了 TTF。",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## 什么是一 .ttf 文件？

带有 .ttf 扩展名的文件表示基于 TrueType 规范字体技术的字体文件。它最初是由 Apple Computer, Inc 为 Mac OS 设计和推出的，后来被 Microsoft 用于 Windows OS。 TrueType 字体在计算机屏幕和打印机上提供最高质量的显示，而不依赖于分辨率。所有使用字体的现代应用程序都可以使用 TTF 文件。 TTF 字体文件可在 Internet 上免费获得，也可以转换为其他字体文件格式，例如 OTF 和 WOFF。

## 历史简介

由 Apply Computer, Inc 在 1980 年代为 MacOS 设计的 TTF 字体格式旨在解决 Adobe 的 Type 1 格式的一些技术限制。 Apple 于 1991 年在 Mac 中加入了对 TrueType 字体的支持。TTF 字体背后的设计目标是存储和处理的效率以及可扩展性。基于这种可扩展性，现有字体可以转换为 TrueType 格式。

1992 年 4 月，在 Apple 同意将 TrueType 授权给 Microsoft 之后，Microsoft 首次在 Windows 3.1 中使用 TrueType 字体。它改进了光栅化机制，提高了它的效率和性能。

## True Type 文件格式规范

TrueType 字体文件是由一系列连接表组成的二进制文件。每个表都是一个单词序列，并有一个称为“标签"的名称。每个标签都是 uint32 数据类型，由四个字符组成。文件中的第一个表是字体目录，可以访问字体文件中的其他表。字体数据包含在字体目录表之后的其他表中。由于每个表都可以通过其标签访问，因此这些表可以在文件中以任何顺序出现。

所需表及其标签名称如下表所示。

|**标签**|**表格**|
---|---|
|'cmap'|字符到字形映射|
|'glyf'|字形数据|
|'头'|字体标题|
|'呵呵'|横标|
|'hmtx'|水平指标|
|'本地'|位置索引|
|'maxp'|最大型材|
|'名字'|命名|
|'发布'|后记|

### 数据类型
TrueType 字体使用下表中列出的标准整数和附加数据类型。

|**数据类型** | **描述** |
---|---|
|短压裂法| 16位有符号小数|
|固定| 16.16位有符号定点数|
|FWord| | 16 位有符号整数，以 FUnits 为单位描述一个量，即 em 空间中的最小可测量距离。
|uFWord| | 16 位无符号整数，描述 FUnits 中的数量，即 em 空间中的最小可测量距离。
|F2Dot14| | 16 位有符号固定数，低 14 位表示小数。
|长日期时间|从 1904 年 1 月 1 日午夜 12:00 开始的以秒为单位的长日期内部格式。它表示为带符号的 64 位整数。

### 字体目录

TrueType 字体中的第一个表是提供对访问其他表中数据所需信息的访问的字体目录。它进一步包括：

* `Offset subtable` - 以字体记录表格并提供偏移信息以访问目录中的每个表格
* `Table Directory` - 包含字体中每个表的条目

#### 偏移子表
偏移子表如下所示。

|**类型**|**名称**|**描述**|
---|---|---|
|uint32|洁牙机类型|指示用于光栅化此字体的 OFA 缩放器的标签；有关更多信息，请参阅下面有关缩放器类型的注释。|
|uint16|表数|桌数|
|uint16|搜索范围| （2 <= numTables 的最大幂）*16|
|uint16|入口选择器| log2（2 <= numTables 的最大幂）|
|uint16|范围移位| numTables*16-searchRange|

#### 表目录
表目录紧跟在偏移子表之后。其结构如下表所示。

|**类型**|**名称**|**描述**|
---|---|---|
|uint32|标签| 4字节标识符|
|uint32|校验和|此表的校验和|
|uint32|偏移| sfnt 开头的偏移量|
|uint32|长度|此表的长度（以字节为单位）（实际长度未填充长度）|

字体文件中的每个表都必须有自己的表目录条目。表中的条目必须按标签升序排序。


## 参考
* [TrueType 字体参考手册](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType 概述](https://learn.microsoft.com/en-us/typography/truetype/)

