---
date: 2020-08-12
keywords: "jxr,.jxr,jxr 文件格式,如何打开 jxr 文件,.jxr 扩展名,jxr 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JXR 文件格式"
linktitle: "JXR"
description: "了解 JXR 文件格式和可以创建和打开 JXR 文件的 API。"
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## 什么是一 .jxr 文件？ ##

JPEG XR（JPEG 扩展范围）是一种用于连续色调照片图像的文件格式。它是一种基于 Microsoft 开发的 HD Photo 的静止图像压缩标准。它支持有损和无损压缩。

## 历史简介 ＃＃

Windows Media Photo 由 Microsoft 在 WinHEC 2006 上首次发布。它于 2006 年 11 月更名为 HD Photo。JPEG XR 于 2009 年 6 月 19 日被批准为国际标准 ISO/IEC 29199-2。ITU-T 和 ISO/IEC 发表了一项议案格式规范 (ITU-T T.833 | ISO/IEC 29199-3)、一致性测试集 (ITU-T T.834 | ISO/IEC 29199-4) 和参考软件 (ITU-T T.835 | ISO /IEC 29199-5) 用于 2010 年图像编码规范完成后的 JPEG XR。描述 JPEG XR 工作流架构的技术报告于 2011 年发布。

## JPEG XR 设计##

与 JPEG 相比，JPEG XR 提供了多项改进，包括：

- **更好的压缩率**：JPEG XR 提供更高的压缩率。
- **无损压缩**：JPEG XR 支持无损压缩。
- **平铺结构**：JPEG XR 图像可以分割成平铺区域，每个区域都可以单独解码。
- **更高的色彩准确度**：JPEG XR 包括到 YCoCg 色彩空间的内部转换，以支持使用 RGB 色彩空间的图像。 JPEG XR 还支持每组件 16 位（每像素 64 位）整数 CMYK 颜色模型。 JPEG XR 支持 HDR 图像的 RGBE 共享指数浮点颜色格式。 JPEG XR 也支持灰度和多通道颜色编码。
- **透明度贴图**：JPEG XR 支持透明度的 alpha 通道。
- **压缩域图像修改**：JPEG XR 图像可以转换为有损编码、降低分辨率、裁剪、翻转、旋转，并且可以在不完全解码文件的情况下更改平铺结构。
- **元数据支持**：JPEG XR 图像文件可能包含 ICC 颜色配置文件，以实现跨多个设备的一致颜色表示。该格式还支持 Exif 和 XMP 元数据格式。

## 容器格式##

JPEG XR 图像数据可以通过使用图像文件目录 (IFT) 标签表以类似 TIFF 的容器格式存储。 JXR 文件在 IFD 标记中包含以下内容：

- 图像数据：它是一个连续的自包含图像数据。
- 可选的 alpha 通道数据：如果存在，则可以单独压缩图像数据，从而支持不支持透明度的应用程序。
- 元数据
- 可选的 XMP 元数据
- 可选的 Exif 元数据

由于它基于 TIFF 格式，因此它继承了所有 TIFF 格式限制，例如 4 GB 文件大小限制。

## 参考 ＃＃

- [JPEG XR - 维基百科](https://en.wikipedia.org/wiki/JPEG_XR)

