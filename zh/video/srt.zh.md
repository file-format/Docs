---
date: 2019-10-11
keywords: "srt, .srt, srt 文件格式, .srt 文件格式, .srt 扩展名, srt 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 SRT 文件格式和可创建和打开 SRT 文件的 API。"
title: "SRT 文件格式"
linktitle: "SRT"
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## 什么是一 .srt 文件？ ##

SRT（SubRip 文件格式）是以 SubRip 文件格式保存的简单字幕文件，扩展名为 .srt。它包含连续编号的字幕、开始和结束时间戳以及字幕文本。 SRT 文件可以在视频内容制作后为其添加字幕。

## SRT 文件结构##

每个字幕在 SRT 文件中有四个部分。

1. 指示字幕编号或位置的数字计数器。
1.-->字符分隔的字幕的开始和结束时间
1. 一行或多行的字幕文本。
1. 表示字幕结束的空行。

### SRT 示例###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

要指定时间 *hours:minutes:seconds,milliseconds (00:00:00,000)* 格式使用。

## SRT 文件的格式化##

SRT 文件的格式源自 HTML 标记。下面列出了 SRT 文件的格式标记。

|效果 |标签 |
| --- | --- |
|粗体|**\ <b>...\</b> ** 或 {b}...{/b}|
|斜体|**\ <i>...\</i> ** 或 **{i}...{/i}**|
|下划线|**\ <u>...\</u> ** 或 **{u}...{/u}**|
|字体颜色|**\ <font color="white">...\</font> **|
|行位置|**{\a3}**（表示文本应该开始出现在第 3 行）

## SubRip 软件##

SubRip 是在 Windows 上运行的免费软件程序。它从不同的视频格式中提取字幕及其时间，并将字幕保存为 SRT 格式。 SubRip 使用光学字符识别从实时视频、其他视频文件和 DVD 中提取字幕。

## 参考 ＃＃

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
