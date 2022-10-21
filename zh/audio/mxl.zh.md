---
date: 2022-03-20
keywords: "mxl,Musepack 文件格式,.mxl 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 MXL 文件格式和可创建和打开 MXL 文件的 API。"
title: "MXL 文件格式 - 压缩的 MusicXML 文件"
linktitle: "MXL"
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## 什么是一 .mxl 文件？

MXL 文件是 MusicXML 文件格式的压缩形式，它是用于交换数字乐谱的开放标准格式。纯文本 MusicXML 文件的大小很大，并且这种文件作为工作表分发格式的使用会受到大文件大小的影响。 [MusicXML](https://www.musicxml.com/) 2.0 通过引入 MXL 文件格式来处理此问题，该格式可压缩文件足以减小文件大小，类似于原始 MIDI 文件。 MXL 文件的推荐媒体类型为 application/vnd.recordare.musicxml。

## MXL 文件格式

MXL 文件存储为带有 .mxl 文件扩展名的 [ZIP](/zh/compression/zip/) 压缩 [XML](/zh/web/xml/) 文件。 MXL 文件使用 [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt) 中指定的 DEFLATE 算法进行压缩。

### MXL 文件结构

每个 MXL 文件都有一个基于 ZIP 的 XML 格式，该格式必须有一个 META-INF/container.xml 文件，该文件描述了该文件的 MusicXML 版本的起点。没有为 MXL 文件格式定义相应的 .xsd 文件。

一个简单的 container.xml 文件的内容如下。此示例取自 MakeMusic 网站上的 Dichterliebe01.mxl 文件。

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
在这个例子中，<container> element 是文档元素。这<rootfiles>元素可以包含一个或多个<rootfile>元素，第一个<rootfile>描述 MusicXML 根的元素。一个 MusicXML 文件用作<rootfile>可能有<score-partwise>,<score-timewise> ， 或者<opus>作为其文档元素。

## 参考

* [压缩 MXL 文件](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

