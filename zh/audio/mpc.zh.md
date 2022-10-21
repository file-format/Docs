---
date: 2021-03-21
keywords: "mpc,Musepack 文件格式,.mpc 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 MPC 文件格式和可创建和打开 MPC 文件的 API。"
title: "MPC - Musepack 音频压缩文件格式"
linktitle: "MPC"
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## 什么是一 .mpc 文件？

带有 .mpc 扩展名的文件是一种 [Musepack](https://musepack.net/) 音频文件格式，它使用音频压缩并强调高质量。这使您甚至可能不会注意到原始 [WAV](/zh/audio/wav/) 文件和压缩 MPC 文件的音质差异。它使用 MPEG-1 Layer-2 算法来实现高度优化的压缩。 Musepack MPC 文件格式是具有 BSD/GNU LGPL 许可证的开源文件。 Musepack 的 [SVN 存储库](http://svn.musepack.net/) 允许获取编解码器的最新更新代码。可以打开 MPC 文件的应用程序包括 VLC 媒体播放器、JetAudio 和 Winamp 以及其他几个。

## MPC 文件格式

MPC 文件使用 MPEG-1 Layer-2 算法来压缩音频文件。它是一种独立于容器的格式，也允许原始流编码。该格式不使用任何内部剪辑，并且可以通过样本精确的剪辑进行流式传输。它的 Packetized 流允许多路复用到音频和视频容器中，例如 [MKV](/zh/video/mkv/)。

## 参考

* [Musepack MPC - 维基百科](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)

