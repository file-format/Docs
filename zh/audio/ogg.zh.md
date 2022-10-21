---
date: 2019-12-13
keywords: "ogg,ogg 文件格式,.ogg 扩展名,ogg 音频格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 OGG 文件格式和可以创建和打开 OGG 文件的 API。"
title: "OGG 文件 - Ogg Vorbis 音频文件"
linktitle: "OGG"
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## 什么是一 .ogg 文件？ ##

OGG 是一个以 .ogg 扩展名保存的 Ogg Vorbis 压缩音频文件。 OGG 文件用于存储音频数据，还可以包含艺术家和曲目信息以及元数据。 OGG 是一种自由开放的容器格式，由 Xiph.Org 基金会维护。

## 历史简介 ＃＃

Ogg 项目于 1993 年作为一个更大项目的一部分开始，并被命名为 Squish，但由于现有商标，它被重命名为 OggSquish。它被描述为为现代音频应用程序创建灵活的压缩音频格式的尝试。 OGG 参考于 2000 年 9 月 2 日从 Vorbis 中分离出来。

由于 OGG 缺乏正式的视频支持，OGM 于 2002 年创建。这允许将来自 Microsoft DirectShow 框架的视频嵌入到基于 OGG 的包装器中。到 2006 年，OGG 得到了许多视频游戏引擎的支持，并且通常用于对免费内容进行编码。自由软件基金会于 2007 年 5 月 15 日开始了一项运动，以增加 Vorbis 作为 MP3 的替代品的使用。到 2009 年 6 月 30 日，OGG 是 Firefox 3.5 的 HTML5 实现支持的唯一容器格式。

## OGG 文件格式##

OGG 格式由数据块组成。每个块称为一个 Ogg 页面。每个页面都以“OggS"开头，以标识 Ogg 格式。标题包含序列号和页码，将每页标识为系列的一部分。该页面由以下组件组成。

- **页眉**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

|位 |价值 |说明 |
| --- | --- | --- |
| 0 | 0x01 |指示页面的第一个数据包是逻辑比特流中前一个数据包的延续。 |
| 1 | 0x02 |指示此页是逻辑比特流中的第一个。 |
| 2 | 0x04 |指示此页是逻辑比特流中的最后一个。 |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **元数据**：VorbisComment 是最广泛支持的元数据存储机制。其他机制包括：
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## 参考 ＃＃

- [OGG - 维基百科](https://en.wikipedia.org/wiki/Ogg)

