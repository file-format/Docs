---
date: 2020-08-12
keywords: "flif, .flif, flif 文件格式, 如何打开 flif 文件, .flif 扩展名, flif 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "FLIF 文件格式"
linktitle: "FLIF"
description: "了解 FLIF 文件格式和可创建和打开 FLIF 文件的 API。"
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## 什么是一 .flif 文件？ ##

FLIF（免费无损图像格式）是一种无损图像格式，其文件使用 .flif 扩展名。 FLIF 声称在压缩率方面优于 [PNG](/zh/image/png/)、无损 [WebP](/zh/image/webp/)、无损 BPG 和无损 JPEG 2000。 FLIF 使用渐进式隔行扫描，因此图像的任何部分下载都可以用作整个图像的有损编码。

## 历史简介 ＃＃

FLIF 于 2015 年 9 月公布，2015 年 10 月发布 alpha 版本。2016 年 9 月，发布了 FLIF 的第一个稳定版本。

## FLIF 设计##

FLIF 使用 CABAC（上下文自适应二进制算术编码）、MANIAC（元自适应近零整数算术编码）的变体进行压缩。 MANIAC 是由 Jon Sneyers 和 Pieter Wuille 开发的熵编码算法。在 MANIAC 中，上下文是在编码时动态学习的决策树节点。这使得上下文模型更加特定于图像并产生更好的压缩。 FLIF 具有以下特点：

- 支持无损压缩
- 通过编码器预处理支持有损压缩
- 支持灰度、RGB 和 RGBA
- 支持每通道 1 到 16 位的颜色深度
- 支持隔行和非隔行文件
- 支持部分下载文件的渐进式解码
- 支持动画
- 支持嵌入式 ICC 颜色配置文件、Exif 和 XMP 元数据
- 对压缩相机原始文件 (RGGB) 的支持有限

## FLIF 文件格式 ##

一个 FLIF 文件有以下四个部分：

## 主标题##

主标题包含主要元数据，包括宽度、高度、颜色深度、帧数。

|类型|数值|描述|
|---|---|---|
|4 字节|"FLIF"|魔术|
|4 位|3 = 仍然； 4 = 我仍然； 5 = 动画； 6 = i 动画|隔行扫描、动画|
|4 位|1 = 灰度； 3 = RGB； 4 = RGBA|通道数 (nb_channels)|
|1 字节|'0','1','2' ('0'=custom)|每通道字节数 (Bpc)|
|varint|width-1|宽度|
|varint|height-1|高度|
|varint|nb_frames-2 (仅当动画)|帧数 (nb_frames)|

## 元数据块##

这部分包含使用 DEFLATE 压缩编码的非像素，如 Exif/XMP 元数据、ICC 颜色配置文件等。这些块的定义类似于 PNG 块，不同之处在于卡盘大小是用可变数量的字节编码的。块的名称可以是 4 个字母（4 个字节）或低于 32 的值，表示非可选块。

以下是可选夹头的示例：

|块名称|描述|内容（DEFLATE-解压后）|
|---|---|---|
|iCCP|ICC 颜色配置文件|原始 ICC 颜色配置文件数据|
|eXif|Exif 元数据|“Exif\0\0"标头后跟 TIFF 标头和 EXIF 数据|
|eXmp|XMP 元数据|包含在没有填充的只读 xpacket 中的 XMP|

### 命名约定###

- **第一个字母**：大写用于关键块，小写用于非关键块。
- **第二个字母**：大写用于公共块，小写用于私有块
- **第三个字母**：大写用于正确显示图像所需的卡盘，而小写对于显示图像并不重要。
- **第四个字母**：大写用于可以安全盲复制的夹头。小写卡盘取决于图像数据。

## 第二个标题##

这包含有关像素实际编码的信息。

|类型|描述|条件|默认值|
|---|---|---|---|
|1 字节|NUL 字节 (0x00)，FLIF16 比特流的块名称||
|uni_int(1,16)|通道每个像素的位数|Bpc == '0'：如果 Bpc == '1'，则重复 (nb_channels)|8，如果 Bpc == '2'，则为 16|
|uni_int(0,1)|标志：alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|循环数|nb_frames > 1||
|uni_int(0,60_000)|以毫秒为单位的帧延迟|nb_frames > 1: 重复(nb_frames)|
|uni_int(0,1)|标志：has_custom_cutoff_and_alpha|||
|uni_int(1,128)|截止|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alpha 除数|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|标志：has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|变量|变换（见下文）|||
|uni_int(1) = 0|指标位：完成变换|||
|uni_int(0,2)|不可见像素预测器|alpha_zero && 隔行扫描 && alpha 范围包括零||

**频道**

|频道号|说明|
|---|----|
|0|红色或灰色|
|1|绿色|
|2|蓝色|
|3|阿尔法|

**转换**

|类型|描述|
|---|---|
|uni_int(1) = 1|指示位：尚未完成|
|uni_int(0,13)|转换标识符|
|变量|变换数据（取决于变换）|

转换用于修改像素数据以实现更好的压缩并跟踪实际出现的像素值。

## 像素数据##

这部分包含使用 MANIAC 熵编码编码的实际像素数据。可以使用隔行或非隔行编码对像素进行编码。

###隔行扫描方法###

在此方法中，定义了缩放级别。缩放级别 0 用于完整图像，缩放级别 1 用于所有偶数行，缩放级别 2 用于缩放级别 1 的所有偶数列。换句话说，每个偶数缩放级别 2k 是下采样版本图像，比例为 1:2^k。缩放级别从最高到最低进行编码。

### 非隔行扫描方法###

在这种方法中，MANIAC 树的编码立即开始，然后是像素的编码。

## 参考 ＃＃

- [FLIF - 维基百科](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

