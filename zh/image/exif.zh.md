{
  "date" : "2019-10-11",
  "keywords" :["exif 文件","exif 文件格式","什么是 exif 文件","文件","exif 示例","exif 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"了解 EXIF 文件格式和可以创建和打开 EXIF 文件的 API。",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .exif 文件？
EXIF 代表“可交换图像文件格式"，该定义最早由 [日本相机工业协会](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) 于 1985 年给出。该标准由日本电子和信息技术产业协会 (JEITA) 截至今天。 EXIF 是主要用于数码相机和扫描仪的图像和声音格式规范的标准。

EXIF 标准包括图像文件的标记和元数据信息。元数据可以包含相机型号、快门速度、日期和时间、光圈、制造商、曝光时间、X 分辨率、Y 分辨率等信息。通常 EXIF 数据默认隐藏。为了查看 EXIF 数据，必须在图像查看应用程序中选择查看属性。 Exif 元数据还可能包括缩略图以及单个图像文件中的技术和主要图像数据。

## 历史和版本##

* 1995年10月，JEIDA建立了Version 1。在这个版本中，JEIDA定义了结构，包括图像数据格式和属性信息，以及基本标签。
* 1997 年 11 月，版本 1.1 引入了版本 1 中的大部分标签，但还添加了可选属性信息和格式操作的规定。
* 1998 年 6 月，版本 2，带有 sRGB 色彩空间、压缩缩略图和音频文件。
* 1998 年 12 月，版本 2.1，具有增强的存储和属性信息。
* 2002 年 2 月，2.2 版，改进了 2.1 版，增加了打印整理功能。
* 2003 年 9 月，版本 2.21，带有可选的色彩空间，称为 adobe RGB。

## EXIF 文件格式

EXIF 使用以下文件格式并添加了特定的元数据。

1. [JPEG](/zh/image/jpeg/) - 用于压缩图像文件的离散余弦变换 (DCT)。
1. [TIFF](/zh/image/tiff/) Rev. 6.0（RGB 或 YCbCr）用于未压缩的图像文件。
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) 用于音频文件（线性 [PCM](https:// /en.wikipedia.org/wiki/Pulse-code_modulation) 或 ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) 用于未压缩音频数据的 μ-Law PCM，以及 [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) 用于压缩音频数据）。

### EXIF 使用的标记###

标记 0xFFE0~~0xFFEF 是“应用标记"，供用户应用使用。例如，较旧的数码相机使用 JFIF（JPEG 文件交换格式）来存储图像。 JFIF 使用 APP0 (0xFFE0) 标记插入数码相机配置数据和缩略图。此外，EXIF 也使用 Application Marker 来插入数据，但 EXIF 使用 APP1 (0xFFE1) Marker 以避免与 JFIF 格式冲突。每种 EXIF 文件格式都是从这种格式开始的。


|SOI 标记|APP1 标记|APP1 数据|其他标记
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

它从 SOI (0xFFD8) Marker 开始，所以它是一个 JPEG 文件。然后 APP1 标记立即跟随。 EXIF的所有数据都存放在这个APP1数据区。上表“SSSS"部分表示APP1数据区（EXIF数据区）的大小。请注意，大小“SSSS"也包括描述符本身的大小。在“SSSS"之后，APP1 数据开始。第一部分是用于识别是否EXIF的特殊数据，使用ASCII字符“EXIF"和2个字节的0x00。在 APP1 标记区域之后，其他 JPEG 标记紧随其后。

### Exif 数据结构###

EXIF 数据（APP1）的粗略结构如下所示。如上所述，EXIF 数据从 ASCII 字符“EXIF"和 2 个字节的 0x00 开始，然后是 EXIF 数据。 EXIF 使用 TIFF 格式存储数据。


|FFE1|APP1 标记
---|---|
|SSSS|APP1 数据|APP1 数据大小
|45786966 0000|Exif 标头
|49492A00 08000000|TIFF 标头
|XXXX。 . . .|IFD0（主图）|目录
|LLLLLLLL|链接到 IFD1
|XXXX。 . . .|IFD0的数据区
|XXXX。 . . .|Exif SubIFD|目录
|00000000|链接结束
|XXXX。 . . .|Exif SubIFD 的数据区
|XXXX。 . . .|IFD1（缩略图）|目录
|00000000|链接结束
|XXXX。 . . .|IFD1的数据区
|FFD8XXXX。 . . XXXXFFD9|缩略图

#### TIFF 标题####

他的 8 字节 [TIFF](/zh/image/tiff/) 文件头包含以下信息：

`Bytes 0-1:` 文件中使用的字节顺序。合法值为：“II"(4949.H)“MM"(4D4D.H)。

在“II"格式中，对于 16 位和 32 位整数，字节顺序始终是从最低有效字节到最高有效字节。这称为 little-endian 字节顺序。在“MM"格式中，对于 16 位和 32 位整数，字节顺序总是从最高有效到最低有效。这称为大端字节序。

`Bytes 2-3:` 一个任意但仔细选择的数字 (42)，进一步将文件标识为 TIFF 文件。字节顺序取决于 Bytes 0-1 的值。

`Bytes 4-7:` 第一个 IFD 的偏移量（以字节为单位）。该目录可以位于文件头之后的任何位置，但必须以单词边界开始。特别是，图像文件目录可能跟随着它所描述的图像数据。读者必须遵循指针可能指向的任何位置。术语字节偏移在本文档中始终用于指代相对于 TIFF 文件开头的位置。文件的第一个字节的偏移量为 0。

#### 图像文件目录####

IFD 包含有关图像的信息以及指向实际图像数据的指针。它由 2 字节的目录条目数（即字段数）组成，然后是一系列 12 字节的字段条目，后跟下一个 IFD 的 4 字节偏移量（如果没有，则为 0）。 TIFF 文件中必须至少有 1 个 IFD，并且每个 IFD 必须至少有一个条目。

##### IFD 条目#####

每个 12 字节的 IFD 条目采用以下格式。


|字节|说明
---|---|
|0-1|标识字段的标签
|2-3|字段类型
|4-7|指定类型的计数
|8-11|Value Offset，该字段的Value的文件偏移量（以字节为单位）。该Value应该从字边界开始；因此，相应的值偏移量将是偶数。此文件偏移量可能指向文件中的任何位置，即使在图像数据之后

TIFF 字段是由 TIFF 标记及其值组成的逻辑实体。这个逻辑概念被实现为一个 IFD 条目，加上实际值（如果它不适合值/偏移部分），即 IFD 条目的最后 4 个字节。在大多数情况下，术语 TIFF 字段和 IFD 条目是可以互换的。

#### 缩略图####

Exif 格式包含图像的缩略图（Ricoh RDC-300Z 除外）。通常它位于 IFD1 旁边。缩略图有 3 种格式； JPEG 格式（JPEG 使用 YCbCr）、RGB TIFF 格式、YCbCr TIFF 格式。

##### JPEG 格式缩略图#####

如果 IFD1 中 Compression(0x0103) Tag 的值为“6"，则缩略图格式为 JPEG。大多数 Exif 图像使用 JPEG 格式的缩略图。在这种情况下，您可以通过 IFD1 中的 JpegIFOffset(0x0201) 标记获取缩略图的偏移量，通过 JpegIFByteCount(0x0202) 标记获取缩略图的大小。数据格式为普通JPEG格式，从0xFFD8开始，到0xFFD9结束。对于 Exif2.1 或更高版本，建议使用 JPEG 格式和 160x120 像素大小的缩略图格式。

##### TIFF 格式缩略图#####

如果 IFD1 中 Compression(0x0103) Tag 的值为 '1'，则缩略图格式为不压缩（称为 TIFF 图像）。缩略图数据的起点是 StripOffset(0x0111) Tag，缩略图的大小是 StripByteCounts(0x0117) Tag 的总和。

## 参考 ＃＃

* [EXIF - 维基百科提供](https://en.wikipedia.org/wiki/Exif)
* [EXIF 文件格式](https://www.media.mit.edu/pia/Research/deepview/exif.html)

