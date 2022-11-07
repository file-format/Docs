---
date: 2019-12-13
keywords: ra,ra ファイル形式,.ra 拡張子,リアル オーディオ ファイル形式,ra オーディオ形式,RealAudio ファイル形式
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RA ファイル形式と,RA ファイルを作成して開くことができる API について学びます。"
title: RA ファイル形式
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## .RA ファイルとは何ですか?

RealAudio (RA) は、Real Networks, Inc. によって開発され、1995 年 4 月にリリースされた独自のオーディオ形式です。ファイルの拡張子は .ra です。低ビットレートとハイファイ オーディオ コーデックを使用します。 RA は、多くのインターネット ラジオ局でインターネット経由のオーディオ ストリーミングに使用されていました。 BBC の Web サイトは 2009 年まで RA を多用していましたが、2011 年 3 月に廃止されました。

## RealNetworks によるファイル拡張子 ##

RealNetworks は、オーディオに RA ファイル形式を使用しました。 RealNetworks は、1997 年にビデオ形式 ([RealVideo](/video/rv/)) の提供を開始しました。拡張子は .rv です。 [RealMedia (RM)](/video/rm/) は、オーディオとビデオのフォーマットの組み合わせに使用されました。最新リリースの RealProduce (Real のエンコーダ) では、ビデオ ファイルに RV 形式が使用され、VBR (Variable bitrate) ビデオ ファイルに [RealMedia Variable Bitrate (RMVB)](/video/rmvb/) 形式が使用されます。

## ストリーミング オーディオ ##

RA はストリーミング メディア形式として開発され、HTTP を使用してストリーミングできます。オーディオ ファイルは、ファイルの最初の部分が受信されるとすぐに再生を開始し、ファイルの残りの部分がダウンロードされるまで再生を続けます。

RealAudio の最初のバージョンでは、独自の PNA または PNM プロトコルを使用してオーディオをストリーミングしていました。その後、IETF 標準化された RTSP (Real Time Streaming Protocol) に切り替えて接続を管理しました。データを送信するには、RDT (Real Data Transfer) プロトコルを使用しました。プロトコルは最初は秘密にされていましたが、後に Helix プロジェクトを通じて一部が公開されました。

RealAudio ファイルをストリーミングするために、ほとんどのページは RAM (Real Audio Metadata) または SMIL (Synchronized Multimedia Integration Language) ファイルにリンクしています。このファイルは、ユーザーのメディア プレーヤーをロードし、ファイルに含まれる URL からオーディオをストリーミングするために使用されます。

## RealAudio オーディオ コーデック ##

以下は、それぞれが 4 文字のコードで識別されるオーディオ コーデックのリストと、それを導入した RealAudio のバージョンです。

|コーデック|RealAudio バージョン|
|---|---|
|lpcJ と 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|料理|6|
|atrc|8|
|raac|9|
|ラップ|10|
|ラルフ|10|

## 参照 ##

- [RealAudio - ウィキペディア](https://en.wikipedia.org/wiki/RealAudio)

