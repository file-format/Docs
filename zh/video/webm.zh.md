---
date: 2019-10-11
keywords: "WEBM,什么是WEBM文件,WEBM文件格式"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 WEBM 文件格式和可以创建和打开 WEBM 文件的 API。"
title: "WEBM - WebM 视频文件格式"
linktitle: "WEBM"
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## 什么是一 .WEBM 文件？

扩展名为 .webm 的文件是基于开放、免版税的 WebM 文件格式的视频文件。它专为在网络上共享视频而设计，并定义了文件容器结构，包括视频和音频格式。 WebM 是 100% 免费的，基于 HTML、HTTP 和 TCP/IP 等开放技术实现高质量，任何人都可以实现。 WebM 专为在 Web 上提供视频而设计，这使得它针对流媒体进行了优化，计算量很小。这使其适合在任何设备上播放视频，尤其是低功耗上网本、手持设备和平板电脑。

## WEBM 文件格式

WebM 文件结构基于 Matroska [MKV](/zh/video/mkv/) 容器文件格式的子集。 WebM 文件中可用的视频流使用压缩效率很高的 VP8 或 VP9 压缩技术进行压缩。同样，WebM 文件中的音频流使用由 [Xiph Foundation] (https://www.xiph.org/) 开发的 Vorbis 或 Opus 编解码器进行压缩。所有这些视频和音频编解码器都是免版税的，可以免费使用。

以下是 WebM 文件格式的摘要规范。

|字段|描述|
---|---|
|MIME 类型 |video/webm|
|纯音频 MIME 类型 |audio/webm|
|统一类型标识符| org.webmproject.webm|
|视频编解码器名称| VP8 或 VP9|
|音频编解码器名称| Vorbis 或 Opus|

### WebM 元素

WebM 是 Matroska 规范的一个子集，为一些 Matroska 功能提供支持。以下是支持的元素的描述。

#### EBML

|名称 |描述|
---|---|
|EBML|设置要遵循的数据的 EBML 特征。每个 EBML 文档都必须以此开头。|
|EBMLVersion |用于创建文件的 EBML 解析器的版本。|
|EBMLReadVersion|解析器必须支持读取此文件的最低 EBML 版本。|
|EBMLMaxIDLength |您将在此文件中找到的 ID 的最大长度（在 Matroska 中为 4 或更少）。|
|EBMLMaxSizeLength|您将在此文件中找到的最大尺寸长度（在 Matroska 中为 8 或更少）。这不会覆盖元素开头指示的元素大小。指示大小大于 EBMLMaxSizeLength 允许的大小的元素应被视为无效。
|DocType|描述此 EBML 标头后面的文档类型的字符串（在我们的例子中为“webm"）。|
|DocTypeVersion|用于创建文件的 DocType 解释器的版本。|
|DocTypeReadVersion|解释器必须支持读取此文件的最低 DocType 版本。|

#### 全局元素

目前，只支持 `Void` 元素，用于使损坏的数据无效，以避免在使用损坏的数据时出现意外行为。内容被丢弃。也用于在子元素中保留空间以供以后使用。

＃＃＃＃ 部分
此元素包含所有其他顶级（级别 1）元素。通常一个 Matroska 文件由 1 个段组成。

#### 元搜索信息

支持以下搜索信息。

|元素名称 |描述|
---|---|
|SeekHead |包含另一个 1 级元素的位置。|
|Seek |包含对 EBML 元素的单个搜索条目。|
|SeekID |与元素名称对应的二进制 ID。|
|SeekPosition |元素在段中的位置，以八位字节为单位（0 = 第一级 1 元素）。|

## 参考

* [WebM](https://www.webmproject.org/)
* [WebM 代码库](https://www.webmproject.org/code/#webp-repositories)

