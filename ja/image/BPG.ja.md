---
date: 2020-08-12
keywords: bpg,.bpg,bpg ファイル形式,bpg ファイルの開き方,.bpg 拡張子,bpg 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG ファイル形式
linktitle: BPG
description: "BPG ファイル形式と,BPG ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## .BPG ファイルとは? ##

BPG (Better Portable Graphics) は、Fabrice Bellard によって 2014 年にデジタル画像用に作成されたファイル形式です。彼は、BPG の方が圧縮効率やサイズ効率が高いため、JPEG の代替として BPG を提案しました。 BPG は、HEVC (High-Efficiency Video Coding) ビデオ圧縮規格のフレーム内エンコーディングを使用します。

BPG は、ハンドヘルド デバイスや IoT デバイスで動作する、ポータブルでメモリ効率の高い形式として設計されています。現在、Web ブラウザは BPG 形式をサポートしていませんが、Web サイトは Bellard によって作成された JavaScript ライブラリを使用して BPG 画像を配信できます。 BPG は、HEVC の Main 4:4:4 16 Still Picture プロファイルをサンプルあたり最大 14 ビットまで使用します。

## 仕様 ##

BPG コンテナー形式は、HEVC で使用される生のビットストリームではなく、一般的な画像形式です。 BPG は、4:4:4、4:2:2、および 4:2:0 のカラー形式をサポートしています。アルファ チャネルは、個別にコード化されたエクストラ チャネルまたは CMYK イメージの 4 番目のチャネルでもサポートされます。 BPG は、Exif、ICC プロファイル、および XMP のメタデータ サポートを提供します。 BPG は、YCbCr (ITU-R BT.601、BT.709、および BT.2020 (一定でない輝度))、YCgCo、RGB、CMYK、およびグレースケール カラー スペースをサポートします。 BGP は、アニメーションと、可逆および可逆の HEVC データ圧縮もサポートしています。

## 参照 ##

- [優れたポータブル グラフィックス - ウィキペディア](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

