{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF2 文件 - Web 开放字体格式 2.0 文件",
  "description":"了解什么是 WOFF2 文件以及可以创建和打开 WOFF2 文件的 API。",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## 什么是 .WOFF2 文件？

WOFF2 是一种字体文件格式，是 Web 开放字体格式 (WOFF) 的压缩程度更高的版本。它被开发为一种减小网络字体文件大小的方法，使它们能够更快地加载并使用更少的带宽。 WOFF2 使用称为 Brotli 的压缩算法来压缩字体数据，这可能导致文件大小明显小于等效的 [WOFF](/zh/font/woff/) 字体。大多数现代网络浏览器都支持这种格式，包括 Chrome、Firefox、Safari、Opera 和 Edge（版本 14 以上）。

## WOFF2 文件格式 - 更多信息

WOFF2 字体文件的内部文件结构由几个不同的部分组成，包括标题、元数据、表目录和字体数据本身。

1. 标头包含有关文件整体格式的信息，包括版本号和文件中存在的表数。

1. 元数据部分包含字体名称、版权和其他与字体相关的信息。

1. 表格目录包含组成字体的不同表格的信息，包括它们在文件中的位置和长度。

1.字体数据本身分为几个不同的表，每个表都包含有关字体的特定信息，例如其字符及其对应的字形。这些表格可能包括：

* 'glyf' 表包含实际的字体轮廓，包括每个字符的形状和大小。
* 'head' 表包含有关字体的一般信息，例如版本号、设计尺寸等。
* 'hmtx' 表包含有关字体规格的信息，包括字符的宽度和位置。
* 每个表格在完成编码过程后被压缩并存储为WOFF2文件格式。

整体结构旨在允许快速解析和解码，以便网络浏览器可以快速有效地加载和显示网站上的字体。

### WOFF2 标头
WOFF 标头包含一个标识签名，指示文件中包含的数据类型。 WOFF 标头及其字段如下所示。

|类型|字段名称|说明|
---|---|---|
|UInt32|签名|0x774F4632 'wOF2' |
|Uint32| flavor |输入字体的“sfnt 版本”。|
|Uint32|长度 |WOFF 文件的总大小。|
|Uint16| numTables |字体表目录中的条目数。|
|Uint16|保留 |保留;设为零。|
|Uint32| totalSfntSize |未压缩字体数据所需的总大小，包括 sfnt 标头、目录和字体表（包括填充）。|
|Uint32| totalCompressedSize 压缩数据块的总长度。|
|Uint16| majorVersion |WOFF 文件的主要版本。|
|Uint16| minorVersion |WOFF 文件的次要版本。|
|Uint32| metaOffset |从 WOFF 文件的开头到元数据块的偏移量。|
|Uint32| metaLength |压缩元数据块的长度。|
|Uint32| metaOrigLength |元数据块的未压缩大小。|
|Uint32| privOffset |从 WOFF 文件开始到专用数据块的偏移量。|
|Uint32| privLength |私有数据块的长度。|


## 参考
* [w3 WOFF2 文件格式](https://www.w3.org/TR/WOFF2/)

