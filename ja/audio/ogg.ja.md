---
date: 2019-12-13
keywords: ogg,ogg ファイル形式,.ogg 拡張子,ogg オーディオ形式
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "OGG ファイル形式と,OGG ファイルを作成して開くことができる API について説明します。"
title: OGG ファイル - Ogg Vorbis オーディオ ファイル
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## .OGG オプション番号

OGG は、.ogg 拡張子で保存される Ogg Vorbis 圧縮オーディオ ファイルです。 OGG ファイルはオーディオ データの保存に使用され、アーティストやトラック情報、メタデータも含めることができます。 OGG は、Xiph.Org Foundation によって管理されている無料でオープンなコンテナー形式です。

## OGG ファイル形式の歴史

Ogg プロジェクトは 1993 年に大規模なプロジェクトの一部として開始され、Squish という名前でしたが、既存の商標のために OggSquish に名前が変更されました。これは、最新のオーディオ アプリケーション向けの柔軟な圧縮オーディオ フォーマットを作成する試みであると説明されました。 OGG リファレンスは、2000 年 9 月 2 日に Vorbis から分離されました。

OGM は、OGG に正式なビデオ サポートがないため、2002 年に作成されました。これにより、Microsoft DirectShow フレームワークのビデオを OGG ベースのラッパーに埋め込むことができました。 2006 年までに、OGG は多くのビデオ ゲーム エンジンでサポートされ、無料コンテンツのエンコードに一般的に使用されました。 Free Software Foundation は 2007 年 5 月 15 日にキャンペーンを開始し、MP3 の優れた代替手段として Vorbis の使用を増やしました。 2009 年 6 月 30 日までに、OGG は Firefox 3.5 の HTML5 実装でサポートされる唯一のコンテナー形式でした。

## OGG ファイル形式

OGG 形式は、データのチャンクで構成されています。各チャンクは Ogg ページと呼ばれます。各ページは、Ogg 形式を識別するために「OggS」で始まります。ヘッダーには、シリーズの一部として各ページを識別するシリアル番号とページ番号が含まれています。このページは、次のコンポーネントで構成されています。

- **ページ ヘッダー**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| |ビット | ビット |値 |説明 |
| | --- | --- | --- |
| | 0 | 0x01 |ページの最初のパケットが、論理ビットストリーム内の前のパケットの続きであることを示します。 | |
| | 1 | 0x02 |このページが論理ビットストリームの最初のページであることを示します。 | |
| | 2 | 0x04 |このページが論理ビットストリームの最後であることを示します。 | |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **メタデータ**: VorbisComment は、メタデータを保存するための最も広くサポートされているメカニズムです。その他のメカニズムには次のものがあります。
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## 参照 ##

- [OGG - ウィキペディア](https://en.wikipedia.org/wiki/Ogg)

