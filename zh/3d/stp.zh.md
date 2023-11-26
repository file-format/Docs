---
date: 2022-01-31
keywords: "stp, .stp, stp 文件格式, 如何打开 stp 文件, .stp 扩展名, stp 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "STP 文件格式"
linktitle: "STP"
description: "了解 STP 文件格式和可创建和打开 STP 文件的 API。"
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## 什么是一 .stp 文件？

STP 文件是用于在 CAD 和 CAM 应用程序之间交换产品数据的 3D CAD 文件。它包含有关 3D 对象的信息，并以类似于 **STEP** 文件格式的方式保存。 STP 文件根据 [STEP](/zh/3d/step/) 应用程序协议 ISO 10303-2xx 促进应用程序之间的数据交换。该 ISO 定义了 EXPRESS 数据建模语言中数据表示的编码机制。 STP 文件可以在 **Autodesk Fusion 360** 等应用程序中打开。

## STP 文件格式 - 更多信息

STP 文件以纯 ASCII 文件格式保存到光盘。这些包含 3D 模型信息作为纯文本，CAD/CAM 应用程序可以读取这些信息以加载这些模型。

STP 文件也以 .step 扩展名保存，由一系列记录组成。这些文件的显着特点包括：

* 字符集定义为 ISO 10646 的代码点。
*“ISO-10303-21；"是第一条记录中的第一个字符。
* 注释被“/*"和“*/"字符包围。
* 最后一条记录包含“END-ISO-10303-21;"如果 STEP 文件符合 2002 版本。
* 如符合2016版，“END-ISO-10303-21"后可能有一个或多个数字签名；终结者。
* 换行符用“\N\"表示，分页符用“\F\"表示。

## 打开 STP 文件

STP 文件可以在 STP 查看器和文本编辑器中打开。

### 使用 STP 查看器打开 STP 文件

各种 CAD 应用程序可以打开 STP 文件以在 Windows、MacOS 和 Linux 上查看。这些包括：

* Autodesk Fusion 360（跨平台）
* FreeCAD（跨平台）
* IMSI TurboCAD (Windows, Mac)
* 达索系统 CATIA（Windows、Linux）

### 使用文本编辑器打开 STP 文件

STP 文件保存为纯文本文件。这使得使用文本编辑器打开 STP 文件成为可能。 Windows 操作系统上的 Notepad 和 Notepad++ 等流行的文本编辑器，以及 MacOS 上的 Apple TextEdit 都可以打开 STP 文件。在文本编辑器中打开后，用户可以编辑 STP 文件的属性。但是，如果更新属性不正确，可能会导致文件损坏。

## 如何转换 STP 文件

有几个应用程序可以将 STP 文件转换为其他文件格式。可以转换 STP 文件的 CAD 应用程序包括：

*欧特克融合360
* IMSI TurboCAD
* 西门子 Solid Edge

除此之外，还有几个在线应用程序可以将 STP 文件转换为其他文件格式。这些在线应用程序可让您将 STP 文件上传到云服务器，然后将它们转换为您想要的格式并返回下载。

Autodesk Fusion 360 可以将 STP 文件转换为以下 3D 和 CAD 文件格式。

* [OBJ](/zh/3d/obj/)
* [3MF](/zh/3d/3mf/)
* [DWG](/zh/cad/dwg/)
* [DXF](/zh/cad/dxf/)
* [ASM](/zh/cad/asm/)
* [IGES](/zh/cad/iges/)
* [STL](/zh/cad/stl/)
* [FBX](/zh/3d/fbx/)
* F3D
* [美元](/zh/3d/usd/)

## 参考

* [ISO 10303-21 - 维基百科](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

