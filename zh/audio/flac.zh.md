---
date: 2019-12-13
keywords: "flac，flac 文件格式，.flac 扩展名，flac 文件，flac 与 mp3"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 FLAC 文件格式和可创建和打开 FLAC 文件的 API。"
title: "FLAC 文件格式"
linktitle: "FLAC"
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## 什么是一 .flac 文件？ ##

FLAC（Free Lossless Audio Codec）是Xiph.Org基金会开发的一种无损压缩音频编码格式。 FLAC 是一种免版税的开放格式，以 .flac 扩展名保存。使用 FLAC 算法压缩的数字音频的大小通常减少到 50% 到 70%。 FLAC 文件可以解压缩为原始音频文件的相同副本。

## FLAC 文件格式

这是 FLAC 比特流的概述。

- **fLaC 标记**：此标记被添加到流的开头。它后面是一个或多个元数据块。
- **元数据块**：FLAC支持128种元数据块；目前定义了以下内容。
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**：音频数据由一个或多个音频帧组成。
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## 历史简介 ＃＃

Josh Coalson 于 2000 年开始开发 FLAC。FLAC 的第一个版本于 2001 年 7 月 20 日发布。FLAC 于 2003 年 1 月 20 日并入 Xiph.Org 旗下。FLAC 的开发被移至 Xiph.Org git 存储库2013 年 3 月 26 日发布 1.3.0 版。

## FLAC项目的组成##

FLAC 项目包括以下内容：

- 流格式。
- 流的简单容器格式（FLAC）。
- libFLAC：参考编码器、解码器和元数据接口库。
- libFLAC++：libFLAC 的面向对象的包装器。
- flac：用于对 FLAC 流进行编码和解码的命令行程序。
- metaflac：FLAC 的命令行元数据编辑器。
- Winamp、XMMX 等音乐播放器的输入插件。
- Ogg 容器格式 (Ogg FLAC)。

## FLAC 设计##

根据音乐的密度和幅度，压缩文件的大小可以比原始文件小 80%。

### 源编码器###

- 它只支持整数样本，不支持浮点。它可以处理每个样本 4 到 32 位的 PCM 位分辨率和 1Hz 到 65,535 Hz 的采样率。 FLAC 编码限制为每个样本 24 位。
- 可以对通道进行分组以利用通道间相关性来增加压缩。
- CRC 校验和用于识别损坏的帧。
- 对于音频样本的转换，FLAC 使用线性预测。

### 元数据###

- FLAC 支持 ReplayGain（用于感知和规范音频中的响度）。
- FLAC 使用与 Vorbis 注释相同的系统进行标记。
- 大多数 FLAC 应用程序使用 libFLAC 进行编码/解码。
- libFLAC API 被组织成流、可搜索的流和文件，以增加对基本 FLAC 比特流的抽象。

＃＃＃ 压缩 ＃＃＃

libFLAC 使用从 0 到 8 的压缩级别，其中 0 是最快的，8 是最慢的压缩级别。尽管在速度和大小之间进行权衡，但压缩文件始终是无损的。

## FLAC 与 MP3
MP3 是一种有损压缩格式，这意味着它可能会在应用压缩后剪切部分音频以减小其大小。而 FLAC 是一种无损文件格式，这意味着您能够以最纯粹的形式听到音频。早期的无损文件格式是 CDA 或 WAV，它们的空间效率不如 FLAC。下表将显示这两种格式之间一些重要术语的比较：

|术语|FLAC|MP3|
---|---|---|
|**数据质量**|没有任何音频数据丢失|压缩音频数据时可能会丢失部分数据|
|**大小**|与有损格式相比，文件大小更大。所以需要更大的存储容量|更小的文件大小，适合在存储空间很小的紧凑型音频设备上播放 |
|**硬件要求**|需要高质量的音频设备和巨大的存储容量|庞大的音频库可以保存在更小的存储空间中。适用于手持设备，如音频播放器或手机|
|**通过 Internet 分发**|由于文件很大，无法在 Internet 上轻松分发 |紧凑的文件大小使其易于在 Internet 上分发|
|**兼容性**|最流行的音乐和音频收听编解码器几乎与地球上的所有设备兼容兼容新一代 PC、手机、AV 接收器、蓝光播放器、Roku 或 Fire TV 等流媒体设备|

## 参考 ＃＃

- [FLAC - 维基百科](https://en.wikipedia.org/wiki/FLAC)

