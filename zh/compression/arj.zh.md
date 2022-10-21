---
date: 2019-12-09
keywords: "arj, .arj, arj 文件格式, 如何打开 arj 文件, .arj 扩展名, arj 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "ARJ 文件格式"
linktitle: "ARJ"
description: "了解 ARJ 文件格式和可创建和打开 ARJ 文件的 API。"
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## 什么是一 .arj 文件？ ##

ARJ (Archived by Robert Jung) 是由 Robert K. Jung 开发的高效压缩存档文件。 ARJ 是在 1990 年代初为 DOS 和早期版本的 Windows 开发的。 ARJ 文件对于备份或共享大量文件很有用，因为您不必跟踪所有这些文件并且只需处理一个文件。 .arj 扩展名用于 ARJ 存档文件。

## ARJ 文件格式##

ARJ 文件包含两种类型的标头：

- 主标题：存档开头有一个主标题。
- 本地标头：本地标头出现在每个文件之前。

|偏移量|类型|计数|描述|
|---|---|---|---|
|0000h|字|1|ID=0EA60h|
|0002h|word|1|基本报头大小|
|0004h|byte|1|标头大小|
|0005h|byte|1|归档器版本号|
|0006h|byte|1|需要的最小版本号|
|0007h|byte|1|主机操作系统：</br> 0 - MS-DOS</br> 1 - 普里莫斯</br>2 - UNIX</br> 3 - 阿米加</br>4 - MAC-OS（系统 xx）</br> 5 - 操作系统/2</br> 6-苹果GS</br> 7 - 雅达利街</br>8 - 下一个</br>9 - VAX VMS|
|0008h|byte|1|内部标志，位图：</br> 0 - 无密码/密码</br>1 - 保留</br>2 - 文件在下一个磁盘上继续</br>3 - 文件起始位置字段可用</br>4 - 路径转换（“\"到“/"）|
|0009h|byte|1|压缩方式：</br> 0 - 存储</br>1 - 压缩最多</br>2 - 压缩</br>3 - 压缩更快</br>4 - 压缩最快|
|000Ah|字节|1|文件类型：</br> 0 - 二进制</br>1 - 7 位文本</br>2 - 评论标题</br>3 - 目录</br>4 - 卷标|
|000Bh|字节|1|保留|
|000Ch|dword|1|MS-DOS 格式的原始文件的日期/时间|
|0010h|dword|1|压缩文件的大小|
|0014h|dword|1|原始文件的大小"|
|0018h|dword|1|原始文件的CRC-32|
|001Ah|word|1|文件名中的文件规范位置|
|001Ch|word|1|文件属性|
|001Eh|word|1|主机数据|
|?|dword|1|扩展文件起始位置|
|????h|dword|1|基本头的CRC-32|
|????h|word|1|第一个扩展头的大小|
|????h+"SIZ"+2|dword|1|扩展头的CRC-32|
|????h+"SIZ"+6|字节|?|压缩文件|

## 参考 ＃＃

- [ARJ - 维基百科](https://en.wikipedia.org/wiki/ARJ)

