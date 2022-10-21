---
date: 2020-08-12
keywords: "bpg, .bpg, bpg 文件格式, 如何打开 bpg 文件, .bpg 扩展名, bpg 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "BPG 文件格式"
linktitle: "BPG"
description: "了解 BPG 文件格式和可创建和打开 BPG 文件的 API。"
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## 什么是一 .bpg 文件？ ##

BPG (Better Portable Graphics) 是 Fabrice Bellard 在 2014 年为数字图像创建的一种文件格式。他提议 BPG 作为 JPEG 的替代品，因为 BPG 的压缩或尺寸效率更高。 BPG 使用 HEVC（高效视频编码）视频压缩标准的帧内编码。

BPG 被设计为一种便携式内存高效格式，适用于手持设备和物联网设备。目前，Web 浏览器不支持 BPG 格式，但网站仍然可以使用 Bellard 编写的 JavaScript 库来传递 BPG 图像。 BPG 使用 HEVC 的 Main 4:4:4 16 静态图片配置文件，每个样本最多 14 位。

## 规格 ＃＃

BPG 容器格式是一种通用图像格式，而不是 HEVC 中使用的原始比特流。 BPG 支持 4:4:4、4:2:2 和 4:2:0 颜色格式。 Alpha 通道也支持单独编码的额外通道或 CMYK 图像的第四通道。 BPG 为 Exif、ICC 配置文件和 XMP 提供元数据支持。 BPG 支持 YCbCr（ITU-R BT.601、BT.709 和 BT.2020（非恒定亮度））、YCgCo、RGB、CMYK 和灰度色彩空间。 BGP 还支持动画以及有损和无损 HEVC 数据压缩。

## 参考 ＃＃

- [更好的便携式图形 - 维基百科](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

