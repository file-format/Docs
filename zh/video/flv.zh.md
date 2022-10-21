---
date: 2019-10-11
keywords: "flv,.flv,flv 文件格式,.flv 文件格式,.flv 扩展名,flv 扩展名,flv 视频格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 FLV 文件格式和可创建和打开 FLV 文件的 API。"
title: "FLV 文件格式"
linktitle: "FLV"
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## 什么是一 .flv 文件？ ##

FLV（Flash 视频）是一种扩展名为 .flv 的容器文件格式。 FLV 用于通过使用 Adobe Flash Player 或 Adobe Air 在 Internet 上传送音频/视频内容。 FLV 文件中的数据的编码方式与 SWF 文件相同。直接支持于 2003 年添加到 Flash Player 7。由于 FLV 的限制，Adobe 系统于 2007 年创建了 F4V。

### 编码###

FLV 文件包含 Sorenson Spark 的视频比特流，它是 H.263 视频标准的专有变体。它是 Flash Player 6 和 7 所需的压缩格式。Flash Player 版本 8 支持 On2 TrueMotion VP6 视频比特流。它是 Flash Player 8 及更高版本的推荐压缩格式。 FLV 支持 MP3、Nellymoser Asao 编解码器和开源 Speex 编解码器中的音频。它还支持未压缩的音频或 ADPCM 格式的音频。 Flash Player 9 的最新版本支持 AAC（HE-AAC/AAC SBR、AAC Main Profile 和 AAC-LC）。

## 结构 ＃＃

FLV 文件由 Header 和 Packets 组成。 FLV 文件以标头开头。标头具有以下字段。

- **签名**：其值为 FLV
- **版本**：默认值为1。只有0x01有效。
- **标志**：0x04 用于音频，0x01 用于视频，因此 0x05 用于音频和视频。
- **Header Size**：默认值为 9。它用于跳过较新的扩展标题。

在标头之后是数据包。 FLV 文件被拆分为多个称为 FLV 标记的数据包，这些数据包具有 15 字节的标头。数据包包含音频、视频、脚本、加密信息和有效负载的元数据。 FLV 数据包具有以下字段。

- **Reserved**：为 FMS 保留，应为 0。
- **Filter**：表示数据包是否被过滤。
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **数据包类型**：这定义了数据包中内容的类型。
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **数据大小**：这表示消息的长度。
- **Timestamp Lower**：以毫秒为单位存储标签数据应用的时间戳。对于第一个数据包，它设置为 NULL。
- **Timestamp Upper**：用于创建 uint32_be 值的扩展。
- **流 ID**：第一个流设置为 NULL。
- **Payload Data**：这是基于数据包类型的数据。

## 参考 ＃＃

- [Flash 视频 - 维基百科](https://en.wikipedia.org/wiki/Flash_Video)

