---
date: 2019-10-11
keywords: flv,.flv,flv ファイル形式,.flv ファイル形式,.flv 拡張子,flv 拡張子,flv ビデオ形式
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLV ファイル形式と,FLV ファイルを作成して開くことができる API について学びます。"
title: FLV ファイル形式
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## .FLV ファイルとは何ですか? ##

FLV (Flash Video) は、拡張子が .flv のコンテナ ファイル形式です。 FLV は、Adobe Flash Player または Adobe Air を使用して、インターネット経由でオーディオ/ビデオ コンテンツを配信するために使用されます。 FLV ファイルのデータは、SWF ファイルと同じ方法でエンコードされます。直接サポートは、2003 年に Flash Player 7 に追加されました。 Adobe システムは、FLV の制限により、2007 年に F4V を作成しました。

### エンコーディング ###

FLV ファイルには、H.263 ビデオ規格の独自仕様である Sorenson Spark のビデオ ビットストリームが含まれています。これは、Flash Player 6 および 7 に必要な圧縮形式です。Flash Player のバージョン 8 は、On2 TrueMotion VP6 ビデオ ビットストリームをサポートしています。これは、Flash Player 8 以降で推奨される圧縮形式です。 FLV は、MP3 のオーディオ、Nellymoser Asao コーデック、およびオープンソースの Speex コーデックをサポートしています。また、非圧縮オーディオまたは ADPCM 形式のオーディオもサポートしています。 AAC (HE-AAC/AAC SBR、AAC メイン プロファイル、および AAC-LC) は、Flash Player 9 の最近のバージョンでサポートされています。

## 構造 ＃＃

FLV ファイルは、ヘッダーとパケットで構成されます。 FLV ファイルはヘッダーから始まります。ヘッダーには次のフィールドがあります。

- **署名**: その値は FLV です
- **バージョン**: デフォルト値は 1 です。0x01 のみが有効です。
- **フラグ**: 0x04 はオーディオに使用され、0x01 はビデオに使用されるため、0x05 はオーディオとビデオの両方に使用されます。
- **ヘッダー サイズ**: デフォルト値は 9 です。新しい展開されたヘッダーをスキップするために使用されます。

ヘッダーの後にパケットが続きます。 FLV ファイルは、15 バイトのヘッダーを持つ FLV タグと呼ばれる複数のパケットに分割されます。パケットには、オーディオ、ビデオ、スクリプト、暗号化情報、およびペイロードのメタデータが含まれています。 FLV パケットには次のフィールドがあります。

- **予約済み**: FMS 用に予約されており、0 にする必要があります。
- **フィルター**: パケットがフィルター処理されているかどうかを示します。
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: これは、パケット内のコンテンツのタイプを定義します。
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **データ サイズ**: メッセージの長さを示します。
- **Timestamp Lower**: タグ データが適用されるタイムスタンプをミリ秒単位で保存します。最初のパケットでは NULL に設定されます。
- **Timestamp Upper**: uint32_be 値を作成するための拡張。
- **ストリーム ID**: 最初のストリームでは NULL に設定されます。
- **ペイロード データ**: これは、パケット タイプに基づくデータです。

## 参照 ##

- [フラッシュ ビデオ - ウィキペディア](https://en.wikipedia.org/wiki/Flash_Video)

