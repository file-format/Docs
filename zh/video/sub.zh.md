{
"date": "2023-06-21",
  "keywords": [
"子文件",
"什么是子文件",
"MicroDVD 字幕文件示例",
"字幕扩展",
"打开子",
"字幕文件类型",
"如何打开SUB文件",
"文件",
"SUB 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "SUB 文件格式 - MicroDVD 字幕文件",
  "description":"了解 SUB 格式以及可以创建和打开 SUB 文件的 API。",
"linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub",
"parent": "video"
}
},
"lastmod": "2023-06-21"
}

## 什么是 .SUB 文件？

SUB 文件是一种 MicroDVD 字幕文件格式,用于在视频中显示字幕,通常具有 .sub 文件扩展名。这些文件包含每个字幕条目的计时信息和文本。

MicroDVD 字幕文件使用简单的基于文本的格式,其中每个字幕条目由几行组成。第一行包含字幕的计时信息,包括开始和结束时间戳。随后的行包含实际的字幕文本。

以下是 MicroDVD 字幕文件的示例：

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## 字幕扩展

字幕可以有各种文件扩展名,具体取决于其格式。一些常见的字幕文件扩展名包括：

- **.srt:** SubRip 字幕格式。它是使用最广泛的字幕格式之一,并受到许多媒体播放器和视频编辑软件的支持。
- **.sub：** 可供不同字幕格式使用的字幕文件格式,例如 MicroDVD,SubViewer 和 SubStation Alpha。
- **.ass 或 .ssa:** Advanced SubStation Alpha 或 SubStation Alpha 字幕格式。它支持文本格式,定位和效果等高级功能。
- **.vtt：** WebVTT（网络视频文本轨道）格式,用于在网络视频上显示字幕。它通常与 HTML5 视频播放器一起使用。
- **.idx/.sub：** DVD 字幕使用的格式。 .idx 文件包含时间和格式信息,而 .sub 文件包含实际的字幕文本。
- **.smi 或 .sami：** 同步可访问媒体交换格式。它通常用于 Windows Media Player 中的隐藏式字幕和字幕。

## 开放式子系统是什么意思？

Open Sub 通常是指 OpenSubtitles,这是一个流行的在线平台,提供多种语言的电影和电视节目字幕。它提供了由其用户社区贡献的大量字幕文件。您可以访问 OpenSubtitles 网站 (www.opensubtitles.org) 搜索并下载您想要的电影或电视剧的字幕。

## 字幕文件类型

字幕文件有多种格式,每种格式都有自己的文件类型或扩展名。以下是一些常见的字幕文件类型：

- **SubRip 字幕格式 (.srt)：** 这是最广泛使用的字幕格式之一。 SRT 文件是纯文本文件,其中包含带时间戳的字幕条目和相应的文本。
- **SubViewer 字幕格式 (.sub)：** SubViewer 文件与 SRT 文件类似,包含带有时间戳和文本的字幕条目,可能支持文本格式和颜色等附加功能。
- **SubStation Alpha (.ssa) 和高级 SubStation Alpha (.ass)：** 这些格式支持文本格式,样式,定位和动画效果等高级功能。 SSA 和 ASS 文件通常用于动漫字幕。
- **MicroDVD 字幕格式 (.sub)：** MicroDVD 格式使用 .sub 文件,并包含每个字幕条目的计时信息和文本。它通常与媒体播放器和视频编辑软件一起使用。
- **DVD 字幕（.sub 和 .idx）：** DVD 字幕通常由两个文件组成：.sub 文件（包含字幕文本）和 .idx 文件（包含时间和格式信息）。
- **WebVTT (.vtt)：** WebVTT 是一种用于网络视频的字幕格式,通常与 HTML5 视频播放器一起使用,并支持基本格式选项。
- **MPL2 字幕格式 (.mpl)：** MPL2 文件与 MPlayer（类 Unix 系统的媒体播放器）一起使用,包含带有时间戳和文本的字幕条目。
- **iTunes 定时文本 (.itt)：** iTunes 定时文本文件用于 Apple iTunes 和其他 Apple 平台中的字幕。它们支持文本样式和定位等功能。
- **图文电视字幕格式（.srt 或 .txt）：** 图文电视字幕通常用于广播电视。它们通常保存为扩展名为 .srt 或 .txt 的纯文本文件。

## 如何打开 SUB 文件？

以下媒体播放器可以将 SUB 文件作为字幕轨道打开。

- VideoLAN VLC 媒体播放器
- MPlayer

要在 VLC 播放器中打开 SUB 文件,请按照下列步骤操作

- 打开 VLC 播放器并播放您的视频
- 从 VLC 媒体播放器菜单栏中,选择 **字幕 > 添加字幕文件 ....**
- 导航到 SUB 文件并打开它

如果您需要编辑 SUB 文件,您可以使用任何文本编辑器打开它,例如 Microsoft Notepad (Windows) 或 Apple TextEdit (Mac)。

## 参考
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

