---
date: 2019-10-11
keywords: "rm,.rm,rm 文件格式,.rm 文件格式,.rm 扩展名,RealMedia 文件格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 RM 文件格式和可以创建和打开 RM 文件的 API。"
title: "RM 文件格式"
linktitle: "R M"
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## 什么是一 .rm 文件？ ##

RealMedia 是由 RealNetworks 开发的专有多媒体容器格式，使用 .rm 扩展名。它与 [RealAudio (RA)](/zh/audio/ra/) 和 [RealVideo(RV)](/zh/video/rv/) 的组合用于通过 Internet 进行流式传输。这些流具有恒定比特率。对于可变比特率，RealNetworks 开发了 RealMedia 可变比特率 (RMVB) 格式。 RealMedia 适用于通过 Internet 流式传输内容，例如可用于流式传输直播电视。

## RealMedia 文件的结构##

RealMedia 文件由一系列块组成，每个块具有以下结构：

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

以下是 RealMedia 文件中存在的块类型：

- **RealMedia 文件头 (.RMF)**：这必须是 RealMedia 文件中的第一个块。一个文件中只存在一个 RMF 块。它包含有关标头数量的信息。
- **文件属性标头 (PROP)**：这包含有关 RealMedia 文件的一般属性的信息。每个 RealMedia 文件中只有一个这种类型的块。
- **媒体属性标头 (MDPR)**：此块包含有关流属性的信息。它包含有关流类型和使用的编解码器的信息。文件中的每个流都有一个 MDPR 块。
- **内容描述标头 (CONT)**：此块包含文本信息，例如 RealMedia 文件中内容的标题或作者。此块仅供参考。
- **数据头（DATA）**：这个块包含一组数据包。
- **索引标头 (INDX)**：此块位于所有 DATA 块之后并包含索引条目。一个文件可以有多个 INDX 块。

## 支持的音视频格式##

### 音频格式###

- lpcJ：RealAudio 1.0（VSELP）
- 28_8：RealAudio 2.0（LD-CELP
- 网络：AC3
- sipr：西普罗
- 厨师：厨师
- atrc：ATRAC3
- ralf：RealAudio 无损格式
- RAAC：LC-AAC
RACP：HE-AAC

### 视频格式###

- CLV1：清晰视频
- RV10：H.263
- RV13：H.263
- RV20：H.263+，RV20
- RV30：H.264 前体
- RV40：H.264 前体，RV40
- RVTR：H.263+ (RV20)

## 参考 ＃＃

- [RealMedia - 维基百科](https://en.wikipedia.org/wiki/RealMedia)

