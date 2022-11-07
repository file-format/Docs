---
date: 2019-10-11
keywords: rm,.rm,rm ファイル形式,.rm ファイル形式,.rm 拡張子,RealMedia ファイル形式
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RM ファイル形式と,RM ファイルを作成して開くことができる API について学びます。"
title: RM ファイル形式
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## .RM オプション番号##

RealMedia は、.rm 拡張子を使用する RealNetworks によって開発された独自のマルチメディア コンテナ フォーマットです。 [RealAudio (RA)](/audio/ra/) と [RealVideo(RV)](/video/rv/) を組み合わせて使用し、インターネット経由でストリーミングします。これらのストリームは固定ビットレートです。可変ビットレート用に、RealNetworks は RealMedia Variable Bitrate (RMVB) フォーマットを開発しました。 RealMedia は、インターネットを介したコンテンツのストリーミングに適しており、ライブ テレビのストリーミングなどに使用できます。

## RealMedia ファイルの構造 ##

RealMedia ファイルは一連のチャンクで構成され、それぞれが次の構造を持っています。

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

以下は、RealMedia ファイルに存在するチャンクのタイプです。

- **RealMedia ファイル ヘッダー (.RMF)**: これは、RealMedia ファイルの最初のチャンクである必要があります。 1 つのファイルには 1 つの RMF チャンクしか存在しません。ヘッダーの数に関する情報が含まれています。
- **ファイル プロパティ ヘッダー (PROP)**: これには、RealMedia ファイルの一般的なプロパティに関する情報が含まれています。各 RealMedia ファイルには、このタイプのチャンクが 1 つだけ存在します。
- **メディア プロパティ ヘッダー (MDPR)**: このチャンクには、ストリーム プロパティに関する情報が含まれます。ストリームのタイプと使用されているコーデックに関する情報が含まれています。ファイル内のストリームごとに 1 つの MDPR チャンクがあります。
- **コンテンツ記述ヘッダー (CONT)**: このチャンクには、RealMedia ファイル内のコンテンツのタイトルや作成者などのテキスト情報が含まれます。このチャンクは情報提供のみを目的としています。
- **データ ヘッダー (DATA)**: このチャンクには、データ パケットのグループが含まれます。
- **インデックス ヘッダー (INDX)**: このチャンクはすべての DATA チャンクの後に続き、インデックス エントリが含まれます。 1 つのファイルに複数の INDX チャンクを含めることができます。

## サポートされているオーディオおよびビデオ形式 ##

### オーディオ形式 ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP)
- dnet: AC3
- sipr: シプロ
- クック: クック
- atrc: ATRAC3
- ralf: RealAudio ロスレス形式
- raac: LC-AAC
ラップ：HE-AAC

### ビデオ形式 ###

- CLV1: クリアビデオ
- RV10: H.263
- RV13: H.263
- RV20: H.263+、RV20
- RV30: H.264 前駆体
- RV40: H.264 プリカーサ、RV40
- RVTR: H.263+ (RV20)

## 参照 ##

- [RealMedia - ウィキペディア](https://en.wikipedia.org/wiki/RealMedia)

