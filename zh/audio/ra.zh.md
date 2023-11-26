---
date: 2019-12-13
keywords: "ra, ra 文件格式, .ra 扩展名, 真实音频文件格式, ra 音频格式, RealAudio 文件格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 RA 文件格式和可创建和打开 RA 文件的 API。"
title: "RA 文件格式"
linktitle: "RA"
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## 什么是一 .ra 文件？ ##

RealAudio (RA) 是由 Real Networks, Inc. 开发并于 1995 年 4 月发布的专有音频格式。它的文件使用 .ra 扩展名。它使用低比特率和高保真音频编解码器。 RA 被许多互联网广播电台用于互联网上的音频流。 BBC 网站在 2009 年之前大量使用 RA，但在 2011 年 3 月停止使用。

## RealNetworks 的文件扩展名##

RealNetworks 将 RA 文件格式用于音频。 RealNetworks 于 1997 年开始提供扩展名为 .rv 的视频格式 ([RealVideo](/zh/video/rv/))。 [RealMedia (RM)](/zh/video/rm/) 用于音频和视频格式的组合。在最新版本的 RealProduce（Real 的编码器）中，RV 格式用于视频文件，而 [RealMedia 可变比特率 (RMVB)](/zh/video/rmvb/) 格式用于 VBR（可变比特率）视频文件。

## 流式音频##

RA 是作为流媒体格式开发的，可以使用 HTTP 进行流式传输。收到文件的第一部分后立即开始播放音频文件，并在下载文件的其余部分后继续播放。

RealAudio 的第一个版本使用专有的 PNA 或 PNM 协议来传输音频。后来他们改用 IETF 标准化的 RTSP（实时流协议）来管理连接。为了发送数据，他们使用了 RDT（真实数据传输）协议。该协议最初是保密的，但后来其中一些通过 Helix 项目公开。

为了流式传输 RealAudio 文件，大多数页面链接到 RAM（Real Audio Metadata）或 SMIL（同步多媒体集成语言）文件。此文件用于加载用户的媒体播放器并从文件中包含的 URL 流式传输音频。

## RealAudio 音频编解码器##

这是一个音频编解码器列表，每个编解码器都由一个四字符代码以及引入它的 RealAudio 版本标识。

|编解码器|RealAudio 版本|
|---|---|
|lpcJ 和 14_4|1|
|28_8|2|
|网络|3|
|SIPR|4/5|
|厨师|6|
|atrc|8|
|raac|9|
|拉普|10|
|拉夫|10|

## 参考 ＃＃

- [RealAudio - 维基百科](https://en.wikipedia.org/wiki/RealAudio)

