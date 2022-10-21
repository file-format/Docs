{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - 高效视频编解码器",
  "description":"了解 IDX 文件格式和可以创建和打开 IDX 文件的 API。",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## 什么是一 .idx 文件？

IDX 文件是一个字幕索引文件，它指向 .sub（VobSub 字幕）文件中的字幕元数据信息列表。它由 VobSub 软件应用程序创建和使用，允许用户从 DVD 中提取字幕并转储到 SUB 文件中。 IDX 文件包含用于指向每个字幕的时间戳和字节偏移。 VobSub 总是与相应的 SUB 文件一起创建一个 IDX 文件。

## IDX 文件格式 - 更多信息

IDX 文件生成并保存为可以在任何文本编辑器中打开的纯文本文件。 IDX 文件包含由媒体播放器读取以读取参数的信息，例如要在屏幕上显示的字幕文本的颜色、字幕文本在屏幕上的位置。

### IDX 字幕设置

典型的 IDX 文件在文件开头存储此元数据信息。字幕设置以 **#** 开头。在所有这些字幕设置之后添加时间戳和图像参考，并以 **timestamp:** 开头。

## IDX 文件格式示例

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## 如何使用 IDX 文件？

如果您有电影的 Sub 和 IDX 文件，您可以播放这些字幕以及为其创建这些字幕的电影。 VLC、GOM Player、PotPlayer 或 PowerDVD 等许多应用程序都能够加载这些 SUB 和 IDX 文件，并与电影一起播放。软件应用程序还可以在 [.mkv](/zh/video/mkv/) 文件中嵌入 SUB 和 IDX 字幕文件。

## 将 IDX 转换为 SRT

[SRT](/zh/video/srt/)（SubRip 文件格式）是以 SubRip 文件格式保存的简单字幕文件。与 VobSub 文件格式相比，它更常用。因此，如果您想将 SUB/IDX 文件转换为 SRT 文件格式，可以使用 3rd 方工具来实现这一点。 SubtitleTools.com 上提供的 SUB/IDX 到 SRT 转换器就是这样一种工具，它将 SUB 和 IDX 文件作为输入并将这些 VobSub 字幕转换为 SRT 文件。

## 参考

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - 维基多媒体](https://wiki.multimedia.cx/index.php?title=VOBsub)

