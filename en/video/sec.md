---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about SEC file format and APIs that can create and open SEC files.
title: SEC File Format - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## What is an SEC file?

A SEC file is a video file that is created with Samsung DVR surveillance system. Video is captured from surveillance cameras and stored to disc in SEC format. The recorded SEC video can be played back with Samsung's video software that can manage video feed from multiple cameras.

## SEC File Format - More Information

SEC files contain h264/AVC stream inside using proprietary file format. The header of an SEC file starts with the model number of the SRD-1670D. The date and time information is held at the end of the file.

### Convert SEC File to AVI

SEC file can be converted to the standard [AVI](/video/avi/) file format using FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## References ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)
- [FFMPEG](http://ffmpeg.zeranoe.com/builds/win32/static/)
