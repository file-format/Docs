---
date: 2019-12-09
keywords: "arc, .arc, arc 文件格式, 如何打开 arc 文件, .arc 扩展名, arc 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "弧文件格式"
linktitle: "弧"
description: "了解 ARC 文件格式和可创建和打开 ARC 文件的 API。"
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## 什么是一 .arc 文件？

ARC 是由 System Enhancement Associates (SEA) 开发的无损数据压缩和归档格式。文件格式和创建它的应用程序都称为 ARC。 ARC 在拨号 BBS 的早期非常流行，因为它在同一个文件中结合了压缩和归档多个文件的功能。 ARC 后来被 [ZIP](/zh/compression/zip/) 取代，它提供了更好的压缩比。

.arc 文件扩展名被其他几种不相关的存档文件类型使用，例如 Internet Archive 用于存储多个 Web 资源的 ARC 格式、FreeArc 存档器使用的不同 ARC 格式、Nintendo 用于资源的不同格式等.

## ARC 文件格式简史

ARC 程序由 System Enhancement Associates 的 Thom Henderson 于 1985 年编写。该程序将文件分组为单个存档文件并压缩它们。 ARC 程序生成的文件使用 .arc 扩展名。 SEA 于 1986 年发布了 ARC 的源代码，ARC 于 1987 年由 Howard Chu 移植到 Unix 和 Atari ST。

Phil Katz 开发了用于归档和提取文件的 PKARC 和 PKXARC。这些文件使用 ARC 文件格式，速度明显更快。与 ARC 不同，Katz 将压缩和归档功能划分为两个不同的文件，从而减少了运行它们的内存需求。

在 SEA 和 Katz 之间的官司之后，SEA 退出了共享软件市场，并开发了具有全屏用户界面的 ARC+Plus。 ARC 格式在 PC 上不再常见。

## 弧文件格式

ARC 文件由一系列文件头和文件组成，后跟归档结束标记，如下所示。

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC 文件头 ###

|偏移量|标签|类型|值|描述|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|方法|
|02|ARCFNT|DS|12|文件名|
|0E| |数据库|00| |
|0F|ARCNSZ|HEX|00000000|压缩后的大小|
|13|ARCDAT|DW|0000|文件日期 (MSDOS)|
|15|ARCTIM|DW|0000|文件时间 (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|未压缩大小|
|1D|ARCFIL|DS|ARCNSZ| |

### 压缩方法###

压缩方法字节指示使用的压缩方法。以下是用于 ARC 文件的压缩方法。

|方法|名称|描述|
|---|---|---|
|0|已存储|未使用压缩|
|1|打包|重复运行长度编码 (RLE)|
|2|压缩|霍夫曼编码|
|3|Crunched|LZW 带 4K 缓冲区，12 位代码|
|4|Crunched|先打包，然后是 12 位 LZW 4K 缓冲区|
|5|Crunched|打包，LZW，4K 缓冲区，可变长度（9-12 位）|
|6|Squashed|LZW，8K 缓冲区，可变长度（9-13 位）|
|7|压碎|打包，然后是 LZW 8K 缓冲区，2-13 位 (PAK 1.0)|
|8|Distill|带有 8K 缓冲区的动态霍夫曼 (PAK 2.0)|

## 参考

- [ARC (文件格式) - 维基百科](https://en.wikipedia.org/wiki/ARC_(file_format))

