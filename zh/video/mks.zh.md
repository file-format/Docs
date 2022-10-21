{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS 文件格式",
  "keywords" :["mks","matroska 视频","mkv 格式","文件","格式","视频"],
  "description":"了解仅由 Matroska 创建的字幕的 MKS 文件格式以及可以创建和打开 MKS 文件的 API。",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## 什么是一 .mks 文件？

MKS 文件通常称为仅包含字幕的 Matroska 文件。虽然 Matroska 是一个通用的文件容器，但它避免保留特定格式的信息。由于在一些音频或视频容器中使用了字幕，Matroska 正在注意存储一些常见的字幕格式。它有助于 Matroska 与增长率保持一致。您需要按照以下几点将字幕存储在 Matroska 中：

- “.mks"。 Matroska 文件将使用该扩展名（仅包含字幕）。
- **CodecPrivate** 用于存储对整个流是全局的所有编解码器相关信息。
- 删除在时间戳本机存储格式中使用的开始和停止时间戳。相反，请使用 Blocks 时间戳和 Duration。
- 您可以使用任何带有透明层的东西，包括视频。

## 常见的字幕格式

以下是有关 Matroska 中存储的更常见字幕格式的一些简要说明：

### 图片字幕
VobSub 字幕格式是第一个导入 Matroska 的图像字幕格式。此格式是通过从 DVD 导出字幕生成的。如果 VobSub 由一组多个流组成，则在存储在 Matroska 中时应将轨道分开。

### SRT 字幕
SRT 是所有字幕格式中最简单和最基本的一种。它由以下四个部分组成：
 



1. 表示字幕顺序的数字。
2.字幕在屏幕上出现和消失的时间。
3. 字幕本身。
4. 一个空行表示下一个字幕的开始。
 



### SSA/ASS 字幕
Sub Station Alpha (SSA) 是流行的字幕编辑器 SubStation Alpha 使用的一种文件格式。 SSA 字幕被粉丝订阅者广泛使用。它具有显示现代特征的能力，例如卡拉OK、定位、造型等。
 



### WebVTT 字幕
万维网联盟 (W3C) 开发了 WebVTT，缩写为“Web Video Text Tracks Format"。此格式用于标记与 HTML 元素相关的外部文本轨道资源。

### HDMV 演示图形字幕
HDMV 演示图形字幕格式 (HDMV PGS) 是一系列位图，我们根本不能说它是文本。换句话说，你可以说它只是一个时间序列的图形图像。为了提取信息，将 PGS 转换为 SRT 是一个必要的过程。

### HDMV文字字幕
HDMV 文本被称为蓝光光盘上使用的文本字幕格式。 Matroska 只允许 UTF-8 字符集存储 TextST 字幕。

### 数字视频广播 (DVB) 字幕
引入 DVB 字幕格式是为了规范电视信号上多种语言字幕的传输和显示。典型的字幕格式还允许任何观众观看 DVB 字幕传输，无论传输系统的制造商是什么。


## 参考 ＃＃

- [Matroska 字幕](https://www.matroska.org/technical/subtitles.html)

