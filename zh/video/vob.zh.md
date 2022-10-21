---
date: 2019-10-11
keywords: "vob,.vob,vob 文件格式,.vob 文件格式,.vob 扩展名,vob 扩展名,vob 视频格式,vob dvd 文件"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 VOB 文件格式和可创建和打开 VOB 文件的 API。"
title: "VOB 文件格式"
linktitle: "VOB"
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## 什么是一 .vob 文件？ ##

VOB 文件通常存储在 DVD 上的 VIDEO_TS 目录中，扩展名为 .vob。 VOB 文件包含视频和音频数据以及菜单和字幕等其他数据。 VOB 基于 MPEG-2 节目流格式，但在私有流中具有额外的限制和规范。 VOB 文件是 MPEG 节目流的严格子集，因此所有 VOB 文件都是 MPEG 节目流，但所有 MPEG 节目流都不符合 VOB。

## DVD 视频的结构##

在计算机上打开 DVD 时，VIDEO_TS 是带有 AUDIO_TS 的顶级目录。 AUDIO_TS 为空且未使用。在 VIDEO_TS 目录中，有 VOB、BUP 和 IFO 文件。 VOB 文件包含 MPEG 内容。它们被分成 1 GB 或更小的块，以便与所有操作系统兼容。 IFO 文件包含有关菜单和标题结构的信息。 BUK 文件是同名 IFO 文件的备份文件。这些文件旨在物理上保存在单独的区域中，以便在 IFO 文件由于 DVD 的物理损坏而损坏的情况下，BUK 文件可以提供相同的信息。

### 物理布局###

- 磁盘上的所有文件必须是连续的。
- 相关文件应彼此相邻（VOB、IFO、BUP）。
- 编号的文件应按升序排列。

## 复制保护##

许多视频 DVD 都经过加密，可以防止从 DVD 复制数据。需要验证和解密密钥来播放位于 DVD 无法访问的导入区域中的文件。这些密钥由 DVD 播放器或软件播放器中的 CSS 解密软件使用。如果没有密钥，则无法播放视频文件，因为打开文件时会请求密钥。

## 参考 ＃＃

- [VOB - 维基百科](https://en.wikipedia.org/wiki/VOB)
- [内部 DVD-Video/目录结构](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

