---
date: 2021-03-21
keywords: "alac,alac 文件格式,.alac 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 ALAC 文件格式和可创建和打开 ALAC 文件的 API。"
title: "ALAC - Apple 无损音频编解码器文件格式"
linktitle: "ALAC"
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## 什么是一 .alac 文件？ ##

ALAC 文件格式是 Apple 无损音频编解码器 (ALAC)，它使用符合 MPEG-4 的 QuickTime 容器。它于 2004 年作为专有文件格式引入，直到 2011 年 Apple 将其开源且免版税。该格式类似于 [FLAC](/zh/audio/flac/)（免费无损音频编解码器），但相对提供更多压缩。它为 [AAC](/zh/audio/aac/) 或 [MP3](/zh/audio/mp3/) 提供了更好的声音替代方案。使用带有 K-Lite 编解码器的 Apple QuickTime、Apple iTunes 和 Micrsoft Windows Media Player 可以打开使用 ALAC 编解码器编码的音频文件。

## ALAC 文件格式

基于 ALAC 编解码器的文件是二进制文件，可作为 [GitHub 上的开源](https://github.com/macosforge/alac) 供开发人员参考。它包含 ALAC 编码器和解码器的源。 Apple 还提供了一个名为“alacconvert"的命令行实用程序，用于在核心音频格式 (CAF) 和 [WAVE](/zh/audio/wav/) 文件中读取和写入音频数据。以下是有关 ALAC 文件格式的一些要点。

1.“位深度"- 16、20、24 和 32 位。
1. `Sample Rate` - 从 1 到 384,000 Hz 的任意整数采样率。可以支持高达 4,294,967,295 (2^32 - 1) Hz 的理论速率。
1. `Packet Size` - 默认数据包大小默认为每个数据包 4096 个音频样本帧。其他数据包大小当然是可能的。但是，不能保证非默认数据包大小在所有支持 Apple Lossless 的硬件设备上都能正常工作。不支持超过 16,384 个样本帧的数据包。
1. `支持的频道` - 它支持一到八个频道。每个通道具有以下信息顺序。

|数陈|订购|
|---|---|
|1 |单声道|
|2 |立体声（左，右）|
|3 |MPEG 3.0 B（中、左、右）|
|4 |MPEG 4.0 B（中、左、右、中环绕）|
|5 |MPEG 5.0 D（中、左、右、左环绕、右环绕）|
|6 |MPEG 5.1 D（中、左、右、左环绕、右环绕、低频效果）|
|7 |Apple AAC 6.1（中、左、右、左环绕、右环绕、中环绕、低频效果）|
|8 |MPEG 7.1 B（中、左中、右中、左、右、左环绕、右环绕、低频效果）|

## 参考

* [ALAC - 维基百科](https://en.wikipedia.org/wiki/Apple_Lossless)
* [苹果无损音频编解码器](https://macosforge.github.io/alac/)
* [macosforge - GitHub 上的 alac](https://github.com/macosforge/alac)

