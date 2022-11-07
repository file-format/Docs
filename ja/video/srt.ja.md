---
date: 2019-10-11
keywords: srt,.srt,srt ファイル形式,.srt ファイル形式,.srt 拡張子,srt 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "SRT ファイル形式と,SRT ファイルを作成して開くことができる API について学びます。"
title: SRT ファイル形式
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## .SRT オプション番号##

SRT (SubRip ファイル形式) は、拡張子が .srt の SubRip ファイル形式で保存された単純な字幕ファイルです。これには、一連の字幕、開始および終了のタイムスタンプ、および字幕テキストが含まれます。 SRT ファイルを使用すると、制作後にビデオ コンテンツに字幕を追加できます。

## SRT ファイルの構造 ##

各サブタイトルには、SRT ファイル内の 4 つの部分があります。

1. サブタイトルの番号または位置を示す数値カウンター。
1. --> 文字で区切られた字幕の開始時間と終了時間
1. 1 行以上の字幕テキスト。
1. 字幕の終わりを示す空白行。

### SRT の例 ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

時間を指定するには、*hours:minutes:seconds,milliseconds (00:00:00,000)* 形式を使用します。

## SRT ファイルのフォーマット ##

SRT ファイルのフォーマットは、HTML タグから派生します。 SRT ファイルのフォーマット タグを以下に示します。

| |効果 |タグ |
| | --- | --- |
|太字|**\ <b>...\</b> ** または {b}...{/b}|
|斜体|**\ <i>...\</i> ** または **{i}...{/i}**|
|下線|**\ <u>...\</u> ** または **{u}...{/u}**|
|フォントの色|**\ <font color="white">...\</font> **|
|行位置|**{\a3}** (テキストが 3 行目から表示されることを示します)

## SubRip ソフトウェア ##

SubRip は、Windows 上で動作するフリー ソフトウェア プログラムです。さまざまなビデオ形式から字幕とそのタイミングを抽出し、字幕を SRT 形式で保存します。 SubRip は光学式文字認識を使用して、ライブ ビデオ、その他のビデオ ファイル、および DVD から字幕を抽出します。

## 参照 ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
