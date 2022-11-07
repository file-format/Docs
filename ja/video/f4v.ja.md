---
date: 2019-10-11
keywords: f4v,.f4v,f4v ファイル形式,.f4v ファイル形式,.f4v 拡張子,f4v 拡張子,f4v ビデオ形式,f4v ファイルを開く方法,f4v ファイルとは
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "F4V ファイル形式と,F4V ファイルを作成して開くことができる API について学習します。"
title: F4V ファイル形式
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## .F4V ファイルとは? ##

F4V (Flash MP4 Video File) は、拡張子 .f4v で保存されたビデオ ファイルです。これは、ISO ベースのメディア ファイル形式 (MPEG-4 Part 12) に基づいています。 [MP4](/video/mp4/) と非常によく似ているため、非公式に Flash MP4 とも呼ばれます。 [FLV](/video/flv/) には、H.264/ACC コンテンツのストリーミング時に制限があり、Adobe Systems が新しい F4V フォーマットを作成する結果となりました。 Flash Player は、Flash Player 9 Update 3 のリリース以降、F4V ファイルを再生できます。

## F4V ファイルの構造 ##

F4V ファイル形式は、ISO ベースのメディア ファイル形式 (MPEG-4 Part 12) に基づいており、MP4 形式に非常に似ています。構造の詳細については、[MP4](/video/mp4/)のページをご覧ください。 F4V と MP4 の主な違いは、F4V が保存できるメタデータ形式です。以下は、F4V 形式でサポートされているメタデータ形式のリストです。

- **タグ ボックス**: ムービー (moov) ボックス内の追加の 4 つのオプションのタグ ボックス (auth、title、dscp、cprt)。
- **XMP メタデータ ボックス**: このボックスは、ムービー (moov) ボックスの直後に表示されます。これにより、ファイルは ActionScript を介して XMP メタデータを SWF ムービーに伝達できます。
- **ilst box**: このボックスはメタ (メタ) ボックス内にあり、多数のメタデータ タグを含めることができます。サポートされているデータ型は次のとおりです。
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **テキスト トラック メタデータ ボックス**: メディア データボックス (mdat) 内のテキスト サンプル (テキストまたは tx3g)。次のメタデータ ボックスを含めることができます。
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## 参照 ##

- [フラッシュ ビデオ - ウィキペディア](https://en.wikipedia.org/wiki/Flash_Video)

