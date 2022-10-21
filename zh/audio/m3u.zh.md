---
date: 2019-12-13
keywords: "m3u, m3u 文件格式, .m3u 扩展名, m3u 多媒体播放列表, m3u 播放列表格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 M3U 文件格式和可创建和打开 M3U 文件的 API。"
title: "M3U 文件格式"
linktitle: "M3U"
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## 什么是一 .m3u 文件？ ##

M3U (MP3 URL) 是一个以 .m3u 扩展名存储的音频播放列表文件。 M3U 不是真正的音频文件，它只是指向音频文件，有时是视频文件。 Fraunhofer 开发了 M3U 以与 Winplay3 软件一起使用。各种媒体播放器和软件也支持它。

## M3U 文件格式##

M3U 文件格式没有官方规范，它是事实上的标准。 M3U 是纯文本文件，如果文本以本地系统的默认非 Unicode 编码编码，则使用 .m3u 扩展名；如果文本采用 UTF-8 编码，则使用 .m3u8 扩展名。 M3U 文件中的每个条目都可以是以下之一：

- 文件的绝对路径
- 相对于 M3U 文件的文件路径。
- 网址

### 扩展 M3U ###

在扩展的 M3U 中，引入了以“#"开头并以冒号 (:) 结尾的附加指令（如果它们有参数）。下面给出了扩展 M3U 的指令列表。

- **#EXTM3U** - 表示扩展 M3U 的文件头，必须是文件的第一行。
- **#EXTENC:** - 文本编码。它必须是文件的第 2 行。
- **#EXTINF:** - 用于轨道信息和其他附加属性。
- **#PLAYLIST:** - 播放列表的标题
- **#EXTGRP:** - 开始名称分组
- **#EXTALB:** - 专辑信息
- **#EXTART:** - 专辑艺术家
- **#EXTGENRE** - 专辑类型
- **#EXTM3A** - 专辑曲目或章节的单个文件播放列表。
- **#EXTBYT:** - 文件大小（以字节为单位）。
- **#EXTBIN:** - 二进制数据如下。
- **#EXTIMG:** - 徽标、封面或其他图像。

### HLS M3U ###

HLS（HTTP Live Streaming）由 Apple 创建，用于将音频和广播流式传输到 iOS 设备。它基于 UTF-8 编码的扩展 M3U。它在 2017 年被 IETF 标准化为 RFC 8216。 HLS 播放列表的标签以“#EXT-X-"开头。下面给出了 HLS 的标签列表

- **EXT-X-VERSION** - 指示基于媒体及其服务器的文件的兼容性版本。
- **#EXT-X-START:** - 表示播放列表的首选起点。
- **#EXT-X-PLAYLIST-TYPE:** - 提供播放列表的类型（EVENT 或 VOD）。
- **#EXT-X-TARGETDURATION:** - 它指定最大段持续时间。
- **#EXT-X-MEDIA-SEQUENCE:** - 表示媒体序列号。
- **#EXT-X-INDEPENDENT-SEGMENTS** - 表示所有媒体样本都是独立的，可以在没有其他片段的情况下进行解码。
- **#EXT-X-MEDIA:** - 用于关联包含相同内容的替代再现的媒体播放列表。
- **#EXT-X-STREAM-INF:** - 它指定作为演绎版一部分的变体流。
- **#EXT-X-BYTERANGE:** - 表示媒体段是由其 URI 标识的资源的子范围。
- **#EXT-X-DISCONTINUITY** - 表示前后媒体片段之间的不连续性。
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - 它允许在同一 Variant Stream 或不同 Variant Streams 的不同再现之间进行同步。
- **#EXT-X-KEY:** - 指定如何解密媒体段。
- **#EXT-X-MAP:** - 指定如何获取媒体初始化部分。需要解析适用的媒体段。
- **#EXT-X-PROGRAM-DATE-TIME:** - 它将媒体段的第一个样本与绝对日期和/或时间相关联。
- **#EXT-X-DATERANGE:** - 它关联一个数据范围。
- **#EXT-XI-FRAMES-ONLY** - 表示播放列表中的每个媒体段都描述了一个 I 帧。
- **EXT-XI-FRAME-STREAM-INF** - 表示播放列表文件包含多媒体演示的 I 帧。
- **#EXT-X-SESSION-DATA:** - 它允许任意会话数据
在主播放列表中进行。
- **#EXT-X-SESSION-KEY:** - 它允许加密密钥。客户端无需先读取播放列表即可预加载这些密钥。
- **#EXT-X-ENDLIST** - 表示不再向文件添加媒体段。

以下是 M3U 使用的互联网媒体类型列表：

- **application/vnd.apple.mpegurl**：它是 M3U 唯一注册的媒体类型（2009 年注册），用于引用 HLS 应用程序中的播放列表。
- 非 HLS 应用程序使用以下 Internet 媒体类型。
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U 示例##

这是 M3U 文件的示例。

```console
#EXTM3U
 
#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3
 
#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## 参考 ＃＃

- [M3U - 维基百科](https://en.wikipedia.org/wiki/M3U)
- [HTTP 直播](https://tools.ietf.org/html/rfc8216)

