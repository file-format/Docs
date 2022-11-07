---
date: 2019-12-13
keywords: flac,flac ファイル形式,.flac 拡張子,flac ファイル,flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLAC ファイル形式と,FLAC ファイルを作成して開くことができる API について学びます。"
title: FLAC ファイル形式
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## FLAC ファイルとは何ですか?

FLAC (Free Lossless Audio Codec) は、Xiph.Org Foundation によって開発されたロスレス圧縮オーディオ コーディング フォーマットです。 FLAC は、.flac 拡張子で保存されるロイヤリティ フリーのオープン フォーマットです。 FLAC アルゴリズムを使用して圧縮されたデジタル オーディオは、通常、サイズが 50 ～ 70% に縮小されます。 FLAC ファイルは、元のオーディオ ファイルの同一のコピーに解凍できます。

## FLAC ファイル形式

これは FLAC ビットストリームの概要です。

- **fLaC マーカー**: このマーカーはストリームの先頭に追加されます。その後に、1 つ以上のメタデータ ブロックが続きます。
- **メタデータ ブロック**: 128 種類のメタデータ ブロックが FLAC でサポートされています。現在、以下が定義されています。
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: オーディオ データは、1 つまたは複数のオーディオ フレームで構成されます。
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## FLAC ファイル形式の歴史

Josh Coalson は 2000 年に FLAC の開発を開始しました。FLAC の最初のバージョンは 2001 年 7 月 20 日にリリースされました。FLAC は 2003 年 1 月 20 日に Xiph.Org フラグの下に組み込まれました。FLAC の開発は、Xiph.Org git リポジトリに移されました。 2013 年 3 月 26 日にバージョン 1.3.0 がリリースされました。

## FLACプロジェクトの構成

FLAC プロジェクトは以下で構成されます。

- ストリーム形式。
- ストリーム用のシンプルなコンテナ形式(FLAC)。
- libFLAC: リファレンス エンコーダー、デコーダー、およびメタデータ インターフェイスのライブラリ。
- libFLAC++: libFLAC のオブジェクト指向ラッパー。
- flac: FLAC ストリームをエンコードおよびデコードするためのコマンドライン プログラム。
- metaflac: FLAC 用のコマンドライン メタデータ エディター。
- Winamp、XMMX などの音楽プレーヤー用の入力プラグイン。
- Ogg コンテナ形式 (Ogg FLAC)。

## FLACデザイン

音楽の密度と振幅によっては、圧縮ファイルのサイズが元のファイルより 80% 小さくなることがあります。

### ソースエンコーダ ###

- 整数サンプルのみをサポートし、浮動小数点はサポートしません。サンプルあたり 4 ～ 32 ビットの PCM ビット解像度と、1 Hz ～ 65,535 Hz のサンプリング レートを処理できます。 FLAC エンコーディングは、サンプルあたり 24 ビットに制限されています。
- チャネルをグループ化して、チャネル間の相関関係を利用して圧縮を高めることができます。
- CRC チェックサムは、破損したフレームを識別するために使用されます。
- オーディオ サンプルの変換には、FLAC は線形予測を使用します。

### メタデータ ###

- FLAC は ReplayGain (オーディオのラウドネスを認識して正規化するために使用) をサポートします。
- FLAC は、タグ付けに Vorbis コメントで使用されるのと同じシステムを使用します。
- libFLAC は、ほとんどの FLAC アプリケーションでエンコード/デコードに使用されます。
- libFLAC API は、ストリーム、シーク可能なストリーム、およびファイルに編成され、ベース FLAC ビットストリームからの抽象化を高めます。

### 圧縮 ###

libFLAC は 0 から 8 までの圧縮レベルを使用します。0 が最も速く、8 が最も遅い圧縮レベルです。速度とサイズのトレードオフはありますが、圧縮ファイルは常にロスレスです。

## FLAC 対 MP3
MP3 は非可逆圧縮形式であるため、圧縮を適用した後にオーディオの一部をカットしてサイズを縮小する場合があります。一方、FLAC は可逆ファイル形式であるため、オーディオを最も純粋な形で聞くことができます。以前の可逆ファイル形式は CDA または WAV であり、FLAC ほどスペース効率が良くありませんでした。次の表は、いくつかの重要な用語について、これら 2 つの形式の比較を示しています。

|用語|FLAC|MP3|
---|---|---|
|**データ品質**|音声データの損失なし|音声データの圧縮時に一部のデータが失われる可能性があります|
|**サイズ**|非可逆形式に比べてファイル サイズが大きくなります。より大きなストレージ容量が必要|ファイル サイズが小さいため、ストレージ容量の少ないコンパクトなオーディオ デバイスでの再生に適しています。
|**ハードウェア要件**|高品質のオーディオ機器と大容量のストレージが必要 |大容量のオーディオ ライブラリを小さなストレージ スペースに保存できます。オーディオ プレーヤーや携帯電話などのハンドヘルド デバイスに適しています|
|**インターネット配信**|ファイルサイズが大きく、インターネット配信が難しい |ファイルサイズが小さいため、インターネット配信がしやすい|
|**互換性**|地球上のあらゆるデバイスとほぼ互換性のある、最も人気のある音楽およびオーディオ リスニング コーデック新世代の PC、電話、AV レシーバー、ブルーレイ プレーヤー、Roku や Fire TV などのストリーミング デバイスと互換性があります|

## 参照 ##

- [FLAC - ウィキペディア](https://en.wikipedia.org/wiki/FLAC)

