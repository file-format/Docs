{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT 文件格式 - 快速电影文件",
  "keywords" :["QT","QuickTime 视频","qt 格式","如何播放 qt 文件","快速电影文件","QTFF","视频","Apple"],
  "description":"了解 QT 文件格式和可以创建和打开 QT 文件的 API。",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## 什么是一 .qt 文件？

扩展名为 .qt 的文件是 QuickTime 框架用来存储多媒体文件内容的多媒体容器文件。由 Apple Inc. 开发的 QuickTime 文件格式 (QTFF) 是一种多媒体容器文件，其中包含音频、视频或文本以供稍后播放。它是在设备、应用程序和操作系统之间交换数字媒体的首选格式。 QT 文件也保存为同样由 Apple Inc. 开发的 [MOV](/zh/video/mov/) 格式。一些可以打开 QT 文件的应用程序包括 Apple QuickTime 播放器、VLC 媒体播放器和 Media Player Classic with K-精简版编解码器包。

## QT 文件格式

QTFF 是面向对象的，它公开了一个灵活的对象集合，以便于解析和扩展。 QT 文件中的每个轨道都包含一个数字编码的媒体流或对位于另一个文件中的媒体流的数据引用。由称为原子的对象组成的分层数据结构充当轨道容器。 [QT文件格式](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)的文件格式规范由Apple Inc官方提供，供开发者参考。

### 媒体描述

QuickTime 文件的媒体描述与媒体数据分开存储。轨道数量、视频压缩格式和时间信息等信息存储在媒体描述（也称为电影资源、电影原子或简称为电影）中。媒体数据由该媒体结构中的索引引用。媒体数据是电影中使用的实际样本数据，例如视频帧和音频样本。

### 原子

Atom 是 QuickTime 文件的基本单元。在任何其他字段之前，任何 atom 中都有两个主要字段：Size 和 Type 字段。 size 字段显示原子的大小，而 type 字段指示存储在原子中的数据类型。从本质上讲，原子是分层的，这意味着一个原子可以包含其他原子，而其他原子仍然可以包含其他原子。示例原子的布局如下图所示。

每个原子有两个部分，标题和数据。标头包含大小和类型字段，数据部分包含实际数据。此外，每个字段解释如下：

#### 原子大小

原子的头部和内容由一个称为原子大小的 32 位整数表示。 size 字段包含原子的大小（以字节为单位），以 32 位无符号整数表示。

#### 原子类型

原子的类型也由一个 32 位整数表示，它主要被视为具有代数的四字符字段，例如电影原子的“moov"（0x6D6F6F76）或“trak"（0x7472616B）一个轨道原子。一旦原子类型已知，它就允许解释其数据。

![alt text](../QT_Sample_Atom.png "QT File Format")

## 文件结构##

QT/MOV 文件由连续的块组成。每个块都有一个 8 字节标头：4 字节块大小（大端，高字节优先）和 4 字节块类型 - 预定义签名之一：“ftyp"、“mdat"、“moov"、“pnot "、"udta"、"uuid"、"moof"、"free"、"skip"、"jP2"、"wide"、"load"、"ctab"、"imap"、"matt"、"kmat"、 “剪辑"、“crgn"、“同步"、“chap"、“tmcd"、“scpt"、“ssrc"、“PICT"。第一个块的类型是“ftype"，并且在偏移量 8 处有一个子类型。 MOV 由必须为“qt"的子类型定义。要编写 MOV 文件，需要迭代块，直到检测到未知类型。

这是一个示例示例：检查示例 MOV 文件的二进制数据，很明显它以偏移量 4 处的签名 **ftyp**（十六进制：66 74 79 70）开始，它定义了 QuickTime 容器文件类型。文件子类型是 **qt~_~_**（十六进制：71 74 20 20），它指向 MOV 文件类型。第一个块大小为 32（十六进制：00 00 00 20，big-endian，高字节在前），大小位于偏移量 0。在偏移量 32（十六进制：20）处位于第二个块，大小为 8 和输入 **mdat**（十六进制：6D 64 61 74）。

下一个块位于偏移量 32+8#40（十六进制：28），大小为 3,263,028（十六进制：00 31 CA 34），在偏移量 44（十六进制）处键入 **mdat**（十六进制：6D 64 61 74） : 2C)。下一个块位于偏移量 40 + 3,263,028#3,263,068（十六进制：00 31 CA 5C），大小为 21,189（十六进制：00 00 52 C5）并在偏移处键入 **moov**（十六进制：6D 6F 6F 76） 1,836,019,574（十六进制：00 31 CA 60）。这是最后一个块，因此总文件大小为 3,263,068+21,189#3,284,257 字节。

## 参考 ＃＃

* [QT 文件格式 - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [QuickTime 文件格式 - 维基百科](https://en.wikipedia.org/wiki/QuickTime_File_Format)

