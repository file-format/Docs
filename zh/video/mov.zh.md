{
  "date" : "2019-10-11",
  "keywords" :[ "mov 文件","mov 文件格式","什么是 mov 文件","文件","mov 示例","mov 文件扩展名","扩展名","格式","QuickTime","MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV 文件 - Apple QuickTime 电影文件格式",
  "description":"了解 MOV 文件格式和可以创建和打开 MOV 文件的 API。",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## 什么是 .mov 文件？

MOV 文件是一种视频文件类型，由 Apple Inc. 开发，包含一个或多个轨道。每个轨道都存储电影、音频、电影剪辑和字幕。它是一个多媒体容器，可以存储不同类型的媒体元素。 MOV 视频格式与 Windows 和 Macintosh 系统兼容。它使用 MPEG-4 编码进行压缩，轨道保存在称为原子的对象中，这些对象放置在分层数据结构中。

## MOV 文件格式简史

MPEG-4 文件格式从 2001 年的 QuickTime 文件格式 (**QTFF**) 规范演变而来。国际标准化组织批准了该格式，并于 1999 年发布了 MPEG-4 第 1 部分系统规范。2001 年，修订文件格式 [MP4](/zh/video/mp4/) 已发布。

MP4 的第一个版本在 2003 年被修订为 MPEG-4 Part 14 (ISO/IEC 14496-14:2003)。 2004 年，MP4 被推广以定义所有基于时间的媒体文件的通用结构。因此，现在它被用作各种其他多媒体文件格式的基础。

## QuickTime 文件格式 (QTFF) - 更多信息

为了与数字多媒体一起工作，QTFF 可以保存多种数据。它是一种数字媒体交换的理念格式，因为该格式定义了描述任何类型媒体结构的标准。文件格式由灵活的面向对象对象集合组成。对于电影在磁盘上的存储，QuickTime 使用了两种结构，即“atoms"和“QTatoms"。

### 原子

Atom 是 QuickTime 文件的基本单元。在任何其他字段之前，任何 atom 中都有两个主要字段：Size 和 Type 字段。 size 字段显示原子的大小，而 type 字段指示存储在原子中的数据类型。从本质上讲，原子是分层的，这意味着一个原子可以包含其他原子，而其他原子仍然可以包含其他原子。示例原子的布局如下图所示。

每个 atom 有两个部分，“header"和“data"。标头包含大小和类型字段，数据部分包含实际数据。此外，每个字段解释如下：

### 原子大小

原子的头部和内容由一个称为原子大小的 32 位整数表示。 size 字段包含原子的大小（以字节为单位），以 32 位无符号整数表示。

### 原子类型

原子的类型也由一个 32 位整数表示，它主要被视为具有代数的四字符字段，例如电影原子的“moov"（0x6D6F6F76）或“trak"（0x7472616B）一个轨道原子。一旦原子类型已知，它就允许解释其数据。

### QT 原子和原子容器

QT atom 提供了一种通用的存储格式，并有一个扩展的 header，由 Size、Type、Atom ID 和 Count of Child atom 字段组成。 QT 原子被包装在一个原子容器中，这是一个独特的数据结构，具有一个带有锁计数的标头。每个原子容器中都有一个根原子，即 QT 原子。 QT atom 的布局如下图所示。

QT atom 容器头有以下数据：

保留：值为 0 的 10 字节元素。

锁定计数：16 位整数，值为 0。

QT atom 标头具有以下数据：

**大小 -** QT atom 标头和内容由 32 位整数以字节表示。在叶原子的情况下，该字段包含单个原子的大小。

**Type -** 原子的类型由一个 32 位整数表示。如果它是根原子，则该值设置为“sean"。

**原子 ID -** 它是一个 32 位整数，显示原子 ID，并且对于所有同级必须是唯一的。根原子总是原子 ID 的值为 1。

**保留 -** 必须设置为 0 的 16 位整数。

**子原子数 -** 一个 16 位整数，表示原子的子原子数。

**保留 -** 必须设置为 0 的 32 位整数。

## MOV文件的文件结构

MOV 文件由连续的块组成。每个块都有一个 8 字节标头：4 字节块大小（大端，高字节优先）和 4 字节块类型 - 预定义签名之一：“ftyp"、“mdat"、“moov"、“pnot "、"udta"、"uuid"、"moof"、"free"、"skip"、"jP2"、"wide"、"load"、"ctab"、"imap"、"matt"、"kmat"、 “剪辑"、“crgn"、“同步"、“chap"、“tmcd"、“scpt"、“ssrc"、“PICT"。第一个块的类型是“ftype"，并且在偏移量 8 处有一个子类型。 MOV 由必须为“qt"的子类型定义。要编写 MOV 文件，需要迭代块，直到检测到未知类型。

这是一个“示例示例"：检查示例 MOV 文件的二进制数据，很明显它以偏移量 4 处的签名 **ftyp**（十六进制：66 74 79 70）开始，它定义了 QuickTime 容器文件类型。文件子类型是 **qt~_~_**（十六进制：71 74 20 20），它指向 MOV 文件类型。第一个块大小为 32（十六进制：00 00 00 20，大端，高字节在前），大小位于偏移量 0。在偏移量 32（十六进制：20）处，位于第二个块，大小为 8 和输入 **mdat**（十六进制：6D 64 61 74）。

下一个块位于偏移量 32+8#40（十六进制：28），大小为 3,263,028（十六进制：00 31 CA 34），在偏移量 44（十六进制）处键入 **mdat**（十六进制：6D 64 61 74） : 2C)。下一个块位于偏移量 40 + 3,263,028#3,263,068（十六进制：00 31 CA 5C），大小为 21,189（十六进制：00 00 52 C5）并在偏移处键入 **moov**（十六进制：6D 6F 6F 76） 1,836,019,574（十六进制：00 31 CA 60）。这是最后一个块，因此总文件大小为 3,263,068+21,189#3,284,257 字节。

## 如何转换 MOV 文件？

有很多媒体播放器和软件视频编辑器可用于将 MOV 文件转换为其他流行的视频文件格式。一些可以将 MOV 文件转换为其他格式的媒体播放器包括：

* VideoLAN VLC 媒体播放器
* Eltima Elmedia 播放器

一些媒体播放器和视频编辑器，包括 VideoLAN VLC 媒体播放器和 Eltima Elmedia Player，可以将 MOV 文件转换为其他格式。这些软件可以将 MOV 文件转换为以下视频格式。

* MPEG-4 视频 - [MP4](/zh/video/mp4/)
* WebM 视频 - [WEBM](/zh/video/webm/)
* 视频传输流 - [TS](/zh/video/ts/)
* 高级系统格式 - [ASF](/zh/video/ts/)
* Ogg Vorbis 音频 - [OGG](/zh/audio/ogg/)
* MP3 音频 - [MP3](/zh/audio/mp3/)
* 免费无损音频编解码器 - [FLAC](/zh/audio/flac/)
* WAVE 音频 - [WAV](/zh/audio/wav/)

## MOV 文件的开源 API

* [React Native API 将 MOV 转换为 MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API 修复 MOV 文件](https://github.com/nrosenstein-stuff/movrepair)
* [将 MOV 转换为 GIF 的 Ruby API](https://github.com/skygroundmedia/convert-mov-to-gif)

## 参考

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

