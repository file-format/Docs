---
date: 2022-01-06
keywords: vtt,.vtt,vtt ファイル形式,.vtt ファイル形式,.vtt 拡張子,vtt 拡張子
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: ".vtt ファイルと,VTT ファイルを作成して開くことができる API について学習します。"
title: VTT ファイル形式 - Web ビデオ テキスト トラック ファイル
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## .VTT オプション番号

VTT ファイルは、Web ビデオ テキスト トラック (WebVTT) 形式を使用して時間指定テキスト トラック (字幕やキャプションなど) を表示するための情報を含むテキスト ファイルです。時間指定テキスト トラックには、字幕やキャプションなどの情報が含まれます。 VTT ファイルの目的は、テキスト オーバーレイを<video>.形式は、SRT ファイルに多少似ています。 WebVTT ベースのテキスト ファイルは、UTF-8 を使用してエンコードされます。 VTT ファイルには、サブタイトル、説明、キャプション、説明、章、メタデータなどの情報が含まれています。 VTT ファイルはプレーン テキスト ファイルであるため、Microsoft Notepad、Apple TextEdit、Notepad++ などのテキスト エディタを使用して開くことができます。

## VTT ファイル形式 - 詳細情報

VTT ファイルは、連続したテキスト トラック情報を保存するために WebVTT ファイル形式を使用します。各タイム テキスト トラックは、次の例に示すように、「キュー」とも呼ばれる 1 行または複数行で構成されます。

### VTT ファイルの例

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT ファイルの構造

以下は、VTT ファイルの構造要件です。

* オプションのバイト オーダー マーク (BOM)。
* 文字列「WEBVTT」。
* WEBVTT の右側にあるオプションのテキスト ヘッダー。
* 2 つの連続する改行に相当する空白行。
*ゼロ以上の手がかりまたはコメント。
* 0 行以上の空白行。

## 参考文献

* [VTT - W3 スクール](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

