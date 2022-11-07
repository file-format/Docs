---
date: 2022-03-25
keywords: sec,.sec,sec ファイル形式,.sec ファイル形式,.sec 拡張子,sec 拡張子
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "SEC ファイル形式と,SEC ファイルを作成して開くことができる API について学びます。"
title: SEC ファイル形式 - Samsung セキュリティ ビデオ ファイル
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## .SEC ファイル拡張子

SEC ファイルは、Samsung DVR 監視システムで作成されたビデオ ファイルです。ビデオは監視カメラからキャプチャされ、SEC 形式でディスクに保存されます。記録された SEC ビデオは、複数のカメラからのビデオ フィードを管理できる Samsung のビデオ ソフトウェアで再生できます。

## SEC ファイル形式 - 詳細情報

SEC ファイルには、独自のファイル形式を使用して内部に h264/AVC ストリームが含まれています。 SEC ファイルのヘッダーは、SRD-1670D のモデル番号で始まります。日付と時刻の情報は、ファイルの末尾に保持されます。

### SEC ファイルを AVI に変換

SEC ファイルは、FFmpeg を使用して標準の [AVI](/video/avi/) ファイル形式に変換できます。

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## 参照 ##

- [Samsung および SEC ファイル](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

