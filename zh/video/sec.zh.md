---
date: 2022-03-25
keywords: "sec,.sec,sec 文件格式,.sec 文件格式,.sec 扩展名,sec 扩展名"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "了解 SEC 文件格式和可创建和打开 SEC 文件的 API。"
title: "SEC 文件格式 - 三星安全视频文件"
linktitle: "证监会"
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## 什么是一 .sec 文件？

SEC 文件是使用三星 DVR 监控系统创建的视频文件。视频从监控摄像头捕获并以 SEC 格式存储到光盘中。可以使用三星的视频软件播放录制的 SEC 视频，该软件可以管理来自多个摄像头的视频馈送。

## SEC 文件格式 - 更多信息

SEC 文件包含使用专有文件格式的 h264/AVC 流。 SEC 文件的标题以 SRD-1670D 的型号开头。日期和时间信息保存在文件的末尾。

### 将 SEC 文件转换为 AVI

SEC 文件可以使用 FFmpeg 转换为标准的 [AVI](/zh/video/avi/) 文件格式。

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## 参考 ＃＃

- [三星和 SEC 文件](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

