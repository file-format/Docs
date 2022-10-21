---
date: 2022-01-06
keywords: "vtt,.vtt,vtt 文件格式,.vtt 文件格式,.vtt 扩展名,vtt 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 .vtt 文件和可创建和打开 VTT 文件的 API。"
title: "VTT 文件格式 - 网络视频文本轨道文件"
linktitle: "VTT"
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## 什么是一 .vtt 文件？

VTT 文件是一个文本文件，其中包含使用 Web 视频文本轨道 (WebVTT) 格式显示定时文本轨道（例如字幕或字幕）的信息。定时文本轨道包括诸如字幕或字幕之类的信息。 VTT 文件的目的是将文本覆盖添加到<video>.格式有点类似于 SRT 文件。基于 WebVTT 的文本文件使用 UTF-8 编码。 VTT 文件包含诸如字幕、描述、标题、描述、章节和元数据等信息。作为纯文本文件，可以使用 Microsoft Notepad、Apple TextEdit 和 Notepad++ 等文本编辑器打开 VTT 文件。

## VTT 文件格式 - 更多信息

VTT 文件使用 WebVTT 文件格式来保存顺序文本轨道信息。每个定时文本轨道由单行或多行组成，也称为“提示"，如下例所示。

### VTT 文件示例

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT 文件结构

以下是 VTT 文件的结构要求。

* 一个可选的字节顺序标记 (BOM)。
* 字符串“WEBVTT"。
* WEBVTT 右侧的可选文本标题。
* 一个空行，相当于两个连续的换行符。
*零个或多个提示或评论。
* 零个或多个空行。

## 参考

* [VTT - W3 学校](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

