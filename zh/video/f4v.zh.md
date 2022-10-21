---
date: 2019-10-11
keywords: "f4v, .f4v, f4v 文件格式, .f4v 文件格式, .f4v 扩展名, f4v 扩展名, f4v 视频格式, 如何打开 f4v 文件, 什么是 f4v 文件"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 F4V 文件格式和可创建和打开 F4V 文件的 API"
title: "F4V 文件格式"
linktitle: "F4V"
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## 什么是一 .f4v 文件？ ##

F4V（Flash MP4 视频文件）是以 .f4v 扩展名保存的视频文件。它基于 ISO 基本媒体文件格式（MPEG-4 Part 12）。它与 [MP4](/zh/video/mp4/) 非常相似，因此也被非正式地称为 Flash MP4。 [FLV](/zh/video/flv/) 在流式传输 H.264/ACC 内容时存在限制，这导致 Adobe Systems 创建了新的 F4V 格式。自 Flash Player 9 Update 3 发布以来，Flash Player 可以播放 F4V 文件。

## F4V 文件的结构##

F4V 文件格式基于 ISO 基本媒体文件格式（MPEG-4 Part 12），与 MP4 格式非常相似。有关结构的详细信息，请参阅 [MP4](/zh/video/mp4/) 页面。 F4V 和 MP4 之间的主要区别在于 F4V 可以存储的元数据格式。下面给出了 F4V 格式支持的元数据格式列表。

- **标签框**：电影 (moov) 框中的附加四个可选标签框（auth、title、dscp、cprt）。
- **XMP 元数据框**：此框紧跟在电影 (moov) 框之后。这样，文件就可以通过 ActionScript 将 XMP 元数据传送到 SWF 影片。
- **ilst box**：此框出现在 Meta（元）框内，可以包含许多元数据标签。支持的数据类型如下所示。
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **文本轨道元数据框**：媒体数据框 (mdat) 内的文本样本（文本或 tx3g）。它可以包含以下元数据框。
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## 参考 ＃＃

- [Flash 视频 - 维基百科](https://en.wikipedia.org/wiki/Flash_Video)

