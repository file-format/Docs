{
"日期":"2023-10-18",
   "keywords":[
"提示",
"提示文件",
"cue cdrwin 提示表文件",
"如何打开提示文件",
"文件",
"提示文件扩展名",
"扩大",
"文件"
],
   "author":{
"display_name":"沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title":"CUE 文件格式 - CDRWIN Cue 表",
   "description":"了解 CUE CDRWIN Cue Sheet 文件格式以及可创建和打开 CUE 文件的 API。",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
"parent":"disc-and-media"
}
},
"lastmod": "2023-10-18"
}

## 什么是 .cue 文件？

**.CUE** 文件，也称为 **CDRWIN Cue Sheet**，是纯文本文件，其中包含有关音频 CD 或光盘映像的轨道和布局的信息，通常采用 BIN 或 ISO 格式。这些文件通常用于描述光盘的结构和内容，使光盘刻录软件或虚拟光驱软件能够准确地再现原始光盘。

## CUE 文件示例

以下是“.cue”文件的示例：

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN 提示表

CDRWIN Cue Sheet 是 CDRWIN 软件使用的“.cue”文件格式的特定变体。 CDRWIN 是 CD/DVD 刻录和创作软件，其“.cue”表专为与该软件一起使用而设计。这些“.cue”表包含 CDRWIN 准确创建或刻录 CD 或 DVD 所需的信息。

以下是 CDRWIN Cue Sheet 的一些关键细节：

1. **CDRWIN 独有**：CDRWIN 的“.cue”表是特定于 CDRWIN 软件的专有格式。虽然它们与标准“.cue”文件有相似之处，但它们是为与 CDRWIN 的功能和设置配合使用而定制的。
    






2. **用户友好的界面**：CDRWIN 提供了一个易于使用的界面来创建和编辑其“.cue”表。用户可以以用户友好的方式添加或修改有关轨道、索引、间隙和其他参数的信息。
    






3. **兼容光盘类型**：CDRWIN Cue Sheets 主要用于创建各种类型的 CD 和 DVD，包括数据光盘、音频 CD、混合模式光盘等。该格式允许用户指定他们想要创建的光盘的类型和内容。
    






4. **控制光盘布局**：CDRWIN Cue Sheets 提供对光盘布局和结构的详细控制，包括曲目顺序、暂停/间隙设置以及用户可能具有的任何其他特定首选项。
    






5. **ISO 和 BIN 支持**：CDRWIN 可以使用 ISO 和 BIN 光盘映像格式。 “.cue”表指定光盘使用哪个图像文件，确保提示和图像之间正确同步。
    






6. **刻录和翻录**：当使用 CDRWIN 刻录光盘或从光盘上翻录曲目时，这些“.cue”表至关重要。它们有助于确保最终产品符合预期的布局和内容。
    






7. **备份和恢复**：CDRWIN 用户在备份 CD 或 DVD 时经常创建“.cue”表。这些表稍后可用于恢复光盘的内容，包括轨道布局和时序。

## 如何打开 CUE 文件？

CDRWIN Cue Sheets 是专门为 CDRWIN 软件设计的，因此它们通常需要在 CDRWIN 中打开和使用。

打开或引用 CUE 文件的程序

-CDRWIN
- 智能项目 IsoBuster
- EZB 系统 UltraISO

## 其他 CUE 文件

以下是使用 **.cue** 文件扩展名的其他文件类型。

**磁盘和媒体**
- [CUE - 提示表文件](/zh/disc-and-media/cue/)
- [CUE - CDRWIN 提示表](/zh/disc-and-media/cue-cdrwin/)

## 参考
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

