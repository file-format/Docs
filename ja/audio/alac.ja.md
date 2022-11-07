---
date: 2021-03-21
keywords: alac,alac ファイル形式,.alac 拡張子
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "ALAC ファイル形式と,ALAC ファイルを作成して開くことができる API について説明します。"
title: ALAC - Apple ロスレス オーディオ コーデック ファイル形式
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## ALAC ファイルとは何ですか?

ALAC ファイル形式は、MPEG-4 準拠の QuickTime コンテナを使用する Apple Lossless Audio Codec (ALAC) です。 2004 年にプロプライエタリなファイル形式として導入され、2011 年に Apple がオープン ソースでロイヤリティ フリーで利用できるようにしました。形式は [FLAC](/audio/flac/) (Free Lossless Audio Codec) に似ていますが、比較的圧縮率が高くなります。 [AAC](/audio/aac/) または [MP3](/audio/mp3/) よりも優れたサウンドの代替手段を提供します。 ALAC コーデックでエンコードされたオーディオ ファイルは、Apple QuickTime、Apple iTunes、および K-Lite コーデックを備えた Micrsoft Windows Media Player を使用して開くことができます。

## ALAC ファイル形式

ALAC コーデックに基づくファイルは、開発者の参照用に [GitHub のオープン ソース](https://github.com/macosforge/alac) として入手できるバイナリ ファイルです。これには、ALAC エンコーダーとデコーダーのソースが含まれています。 Apple は、Core Audio Format (CAF) および [WAVE](/audio/wav/) ファイルとの間でオーディオ データを読み書きするための、「alacconvert」と呼ばれるコマンド ライン ユーティリティも提供しています。以下は、ALAC ファイル形式に関する重要なポイントです。

1.「ビット深度」 - 16、20、24、および 32 ビット。
1. 「サンプル レート」 - 1 ～ 384,000 Hz の任意の整数サンプル レート。最大 4,294,967,295 (2^32 - 1) Hz の理論上のレートをサポートできます。
1. 「パケット サイズ」 - デフォルトのパケット サイズは、パケットあたり 4096 サンプル フレームのオーディオにデフォルト設定されています。他のパケット サイズももちろん可能です。ただし、デフォルト以外のパケット サイズは、Apple Lossless をサポートするすべてのハードウェア デバイスで適切に動作することが保証されているわけではありません。 16,384 サンプル フレームを超えるパケットはサポートされていません。
1. 「対応チャンネル」 - 1 ～ 8 チャンネルをサポートします。各チャネルには、次の順序の情報があります。

|ナムチャン|注文|
|---|---|
|1 |モノ|
|2 |ステレオ (左、右)|
|3 |MPEG 3.0 B (中央、左、右)|
|4 |MPEG 4.0 B (中央、左、右、中央サラウンド)|
|5 |MPEG 5.0 D (中央、左、右、左サラウンド、右サラウンド)|
|6 |MPEG 5.1 D (中央、左、右、左サラウンド、右サラウンド、低周波効果)|
|7 |Apple AAC 6.1 (センター、左、右、左サラウンド、右サラウンド、センター サラウンド、低周波効果)|
|8 |MPEG 7.1 B (中央、左中央、右中央、左、右、左サラウンド、右サラウンド、低周波効果)|

## 参考文献

* [ALAC - ウィキペディア](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - GitHub の alac](https://github.com/macosforge/alac)

