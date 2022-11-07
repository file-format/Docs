---
date: 2019-10-11
keywords: WEBM, WEBMファイルとは, WEBMファイル形式
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "WEBM ファイル形式と,WEBM ファイルを作成して開くことができる API について学習します。"
title: WEBM - WebM ビデオ ファイル形式
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## .WEBM オプション番号

拡張子が .webm のファイルは、ロイヤリティ フリーのオープンな WebM ファイル形式に基づくビデオ ファイルです。 Web 上でビデオを共有するために設計されており、ビデオおよびオーディオ形式を含むファイル コンテナー構造を定義します。 WebM は 100% 無料で、誰でも実装できる HTML、HTTP、TCP/IP などのオープン テクノロジーに基づいた高品質の実装です。 WebM は、Web 上でビデオを提供するために特別に設計されているため、少ない計算フットプリントでストリーミング用に最適化されています。これにより、あらゆるデバイス、特に低電力のネットブック、ハンドヘルド、タブレットでのビデオ再生に適しています。

## WEBMファイル形式

WebM ファイル構造は、Matroska [MKV](/video/mkv/) コンテナー ファイル形式のサブセットに基づいています。 WebM ファイルで利用可能なビデオ ストリームは、圧縮効率の高い VP8 または VP9 圧縮テクノロジを使用して圧縮されます。同様に、WebM ファイルのオーディオ ストリームは、[Xiph Foundation](https://www.xiph.org/) によって開発された Vorbis または Opus コーデックを使用して圧縮されます。これらのビデオとオーディオ コーデックはすべてロイヤリティ フリーであり、無料で使用できます。

以下は、WebM ファイル形式の仕様の概要です。

|フィールド|説明|
---|---|
|MIME タイプ |video/webm|
|音声のみの MIME タイプ |audio/webm|
|ユニフォーム型識別子| org.webmproject.webm|
|ビデオコーデック名| VP8 または VP9|
|オーディオコーデック名| Vorbis または Opus|

### WebM 要素

Matroska 仕様のサブセットである WebM は、Matroska 機能の一部をサポートします。以下は、サポートされている要素の説明です。

#### EBML

|名前 |説明|
---|---|
|EBML|従うデータの EBML 特性を設定します。各 EBML ドキュメントはこれで開始する必要があります。|
|EBMLVersion |ファイルの作成に使用された EBML パーサーのバージョン。|
|EBMLReadVersion|このファイルを読み取るためにパーサーがサポートする必要がある最小 EBML バージョン。|
|EBMLMaxIDLength |このファイルにある ID の最大長 (Matroska では 4 以下) |
|EBMLMaxSizeLength|このファイルにあるサイズの最大長 (Matroska では 8 以下)。これは、要素の先頭に示されている要素サイズをオーバーライドしません。 EBMLMaxSizeLength で許可されているサイズよりも大きい指定サイズを持つ要素は、無効と見なされます。|
|DocType|この EBML ヘッダーに続くドキュメントのタイプを表す文字列 (この場合は「webm」)。
|DocTypeVersion|ファイルの作成に使用された DocType インタープリターのバージョン。|
|DocTypeReadVersion|インタープリターがこのファイルを読み取るためにサポートする必要がある最小 DocType バージョン。|

#### グローバル要素

現時点では、破損したデータを使用する際の予期しない動作を回避するために、破損したデータを無効にするために使用される `Void` 要素のみがサポートされています。コンテンツは破棄されます。後で使用するためにサブ要素にスペースを確保するためにも使用されます。

#### セグメント
この要素には、他のすべての最上位 (レベル 1) 要素が含まれます。通常、Matroska ファイルは 1 つのセグメントで構成されます。

#### メタシーク情報

以下のシーク情報がサポートされています。

|要素名 |説明|
---|---|
|SeekHead |別のレベル 1 要素の位置を含みます。|
|Seek |EBML 要素への単一のシーク エントリを含みます。|
|SeekID |要素名に対応するバイナリ ID。|
|SeekPosition |セグメント内の要素の位置 (オクテット単位) (0 = 最初のレベル 1 要素)。

## 参考文献

* [WebM](https://www.webmproject.org/)
* [WebM コード レポジトリ](https://www.webmproject.org/code/#webp-repositories)

