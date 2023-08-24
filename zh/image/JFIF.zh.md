---
date: 2020-08-12
keywords: "jfif,.jfif,jfif 文件格式,如何打开 jfif 文件,.jfif 扩展名,jfif 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JFIF 文件 - 什么是 .jfif 文件？"
linktitle: "JFIF"
description: "了解 JFIF 文件格式和可以创建和打开 JFIF 文件的 API。"
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## 什么是一 .jfif 文件？

JFIF（JPEG 文件交换格式 (JFIF)）是一种使用 .jfif 扩展名的图像格式文件。 JFIF 通过降低复杂性并解决其局限性构建在 JIF（JPEG 交换格式）之上。

## JFIF简史

JFIF 文档开发由 Eric Hamilton 领导，并于 1991 年底就第一个版本达成协议。1.02 版于 1992 年 9 月 7 日发布。RFC 2046 指定 JFIF 格式用于通过 Internet 传输 JPEG 图像。 JFIF 于 2009 年由 ECMA 发布，并于 2011 年被 ITU-T 标准化为 T.871 建议书，并于 2013 年被 ISO/IEC 标准化为 ISO/IEC 10918-5

## JFIF 文件格式##

JFIF 文件由 JPEG 标准第 1 部分中定义的一系列标记组成。每个标记由两个字节组成（FF 后跟一个指定标记类型的字节）。标记可以是独立的，也可以指示标记段的开始。

JFIF 允许 Y、Cb、Cr 等多个组件具有不同的分辨率，但未定义它们的对齐方式。与 JPEG 不同，JFIF 可以提供分辨率和纵横比信息。 JFIF 还定义了要使用的颜色模型。

### 文件结构##

|段|代码|说明|
|---|---|---|
|SOI|FF D8|图像开始|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|其他标记段|
|SOS|FF DA|扫描开始|
||压缩图像数据||
|EOI|FF D9|图片结尾|

JFIF 标准定义了以下部分：

### JFIF APP0 标记段###

它是包含图像参数的强制段。它还可以包含嵌入的未压缩缩略图。

|字段|大小（字节）|描述|
|---|---|---|
|APP0 标记|2|FF E0|
|长度|2|不包括 APP0 标记的段长度|
|标识符|5|以空字节结尾的 ASCII 格式的 JFIF (4A 46 49 46 00)|
|JFIF 版本|2|JFIF 版本|
|密度单位|1|以下像素密度字段的单位</br>00：无单位； width:height 像素纵横比等于 Ydensity:Xdensity</br> 01：每英寸像素</br>02 : 每厘米像素数|
|Xdensity|2|大于零的水平像素密度|
|Ydensity|2|大于零的垂直像素密度|
|Xthumbnail|1|嵌入的 RGB 缩略图的水平像素数。可能为零|
|Ythumbnail|1|嵌入的 RGB 缩略图的垂直像素数。可能为零|
|缩略图数据|3 × n|未压缩的 24 位 RGB 光栅缩略图数据|

### JFIF 扩展 APP0 标记段###

这是一个可选部分，如果已定义，则必须紧跟在 JFIF APP0 标记段之后。 JFIF 1.02 及更高版本支持此部分，并允许嵌入三种不同格式的缩略图。

|字段|大小（字节）|描述|
|---|---|---|
|APP0 标记|2|FF E0|
|Length|2|不包括 APP0 标记的段长度|
|标识符|5|以空字节结尾的 ASCII 格式的 JFXX (4A 46 58 58 00)|
|缩略图格式|1|指定用于以下嵌入缩略图的数据格式：</br> 10：JPEG格式</br>11 : 每像素 1 字节的调色板格式</br>13：每像素 3 字节 RGB 格式|
|缩略图数据|变量||

## JFIF 到其他图像文件格式的转换

JFIF 可以转换为流行的图像文件格式，例如 [PNG](/zh/image/png/)、[JPG](/zh/image/jpeg/) 和 [PDF](/zh/pdf/)。

## 参考 ＃＃

- [JFIF - 维基百科](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

