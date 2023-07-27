{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - マテリアル交換フォーマット",
  "keywords" :[ "MXF", "matroska ビデオ", "mkv 形式", "MXF ファイルの再生方法", "SMPTE", "マルチメディア", "ビデオ" ],
  "description":"MXF ファイル形式と,MXF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## MXF ファイルとは何ですか?

拡張子が .mxf のファイルは、ファイルに関するメタデータ情報と共にデジタル ビデオおよびオーディオ メディアを含むマルチメディア コンテナー形式です。 SMPTE (Society of Motion Picture and Television Engineers) 規格に準拠しています。この規格は、メディアおよびエンターテイメント業界で働くエンジニアリング、テクノロジー、エグゼクティブの専門家の世界的な協会です。 MXF ファイルは、[AVI](/video/avi/) や [MOV](/video/mov/) などの他のファイル形式に変換できます。

## MXF ファイル形式

MXF ファイルは、実際には、明確な形式の一連のバイトで構成されるバイナリ ファイルです。デコード アプリケーションは、この形式を理解し、そこから情報を抽出するために、この形式に準拠する必要があります。この形式では、以下で説明する KLV コーディングを使用して、下位互換性を損なうことなく新しいアイテムを追加できます。

* キー – 要素の識別子、SMPTE ユニバーサル ラベル (UL)
* 長さ – この項目に必要なスペースの量を減らすために使用される可変長エンコーディングであるデータの長さ
* 値 – 要素の実際の値。

### SMPTEフォーマット仕様

MXF ファイル形式は、次の SMPTE 仕様で定義されています。

* SMPTE ST 377-1:2011。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — ファイル形式の仕様
* SMPTE ST 377-2 (2012 年 1 月現在進行中)。 MXF の KLV エンコード拡張構文。
* SMPTE ST 378:2004 (アーカイブ 2010)。テレビ — MXF (Material Exchange Format) — 運用パターン 1a (単品、単品)
* SMPTE ST 379-1:2009。 Material Exchange Format (MXF) — MXF 汎用コンテナ
* SMPTE ST 379-2:2010。 Material Exchange Format (MXF) -- MXF Constrained Generic Container
* SMPTE ST 380:2004。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — 記述的メタデータ スキーム 1 (標準、動的)
* SMPTE ST 381-1:2005。 Television — Material Exchange Format (MXF) — MPEG ストリームを MXF Generic Container (Dynamic) にマッピングする
* SMPTE ST 381-2:2011。 Material Exchange Format (MXF) — MPEG ストリームを MXF Constrained Generic Container にマッピングする
* SMPTE ST 382:2007。 Material Exchange Format (MXF) — AES3 ストリームとブロードキャスト ウェーブ オーディオを MXF ジェネリック コンテナーにマッピングする
* SMPTE ST 383:2008。 Television — Material Exchange Format (MXF) — DV-DIF データを MXF Generic Container にマッピングする
* SMPTE ST 384:2005。 Television — Material Exchange Format (MXF) — 非圧縮画像の MXF ジェネリック コンテナへのマッピング
* SMPTE ST 385:2004。 Television — Material Exchange Format (MXF) — SDTI-CP エッセンスとメタデータを MXF ジェネリック コンテナーにマッピングする
* SMPTE ST 386:2004 (アーカイブ 2010)。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — タイプ D-10 エッセンス データを MXF ジェネリック コンテナにマッピング
* SMPTE ST 387:2004 (アーカイブ 2010)。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — タイプ D-11 エッセンス データを MXF ジェネリック コンテナにマッピング
* SMPTE ST 388:2004 (アーカイブ 2010)。 Television — Material Exchange Format (MXF) — A-law コード化されたオーディオを MXF ジェネリック コンテナにマッピングする
* SMPTE ST 389:2005。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — MXF ジェネリック コンテナ リバース プレイ システム要素
* SMPTE ST 390:2011。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — 特殊な操作パターン「アトム」 (単一アイテムの簡略化された表現)
* SMPTE ST 391:2004 (アーカイブ 2010)。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — 運用パターン 1b (単品、連動パッケージ)
* SMPTE ST 392:2004。テレビ — MXF (マテリアル エクスチェンジ フォーマット) — 運用パターン 2a (プレイリスト アイテム、単一パッケージ)
* SMPTE ST 393:2004。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — 運用パターン 2b (プレイリスト アイテム、連動パッケージ)
* SMPTE ST 394:2006。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — MXF ジェネリック コンテナのシステム スキーム 1
* SMPTE ST 405:2006。テレビ — マテリアル エクスチェンジ フォーマット (MXF) — MXF ジェネリック コンテナ システム スキーム 1 の要素と個々のデータ項目
* SMPTE ST 407:2006。テレビ — MXF — 運用パターン 3a および 3b
* SMPTE ST 408:2006。テレビ — MXF — 運用パターン 1c、2c、および 3c
* SMPTE ST 410: 2008. Material Exchange Format - Generic Stream Partition。
* SMPTE ST 422:2006。 Material Exchange Format — JPEG2000 コードストリームを MXF ジェネリック コンテナにマッピングする
* SMPTE ST 429.4:2006。 D シネマ パッケージ — MXF JPEG 2000 アプリケーション
* SMPTE ST 429.5:2006。 D シネマ パッケージ — 時間指定テキスト トラック ファイル
* SMPTE ST 429.6:2006。 D シネマ パッケージ — MXF トラック ファイル エッセンスの暗号化
* SMPTE ST 434:2006。 Material Exchange Format — メタデータとファイル構造情報の XML エンコーディング
* SMPTE ST 436:2006。テレビ — VBI ラインと補助データ パケットの MXF マッピング
* SMPTE ST 2019-4:2009。 VC-3 コーディング ユニットを MXF ジェネリック コンテナにマッピングする
* SMPTE ST 2037:2009。 VC-1 を MXF 汎用コンテナにマッピングする
* SMPTE RP 2008:2008。 Material Exchange Format — AVC ストリームを MXF 汎用コンテナにマッピングする
* SMPTE RP 2057:2011。 MXF でのテキストベースのメタデータ キャリッジ
* SMPTE EG 41:2004。 Material Exchange Format (MXF) — エンジニアリング ガイドライン。注: このドキュメントは、2012 年 1 月に閲覧した時点で SMPTE Web サイトに掲載されていませんでした。
* SMPTE EG 42:2004。 Material Exchange Format (MXF) — MXF 記述メタデータ
* SMPTE RDD 3:2008。 e-VTR MXF 相互運用性仕様
* SMPTE RDD 9-2009。 Sony MPEG Long GOP 製品の MXF 相互運用性仕様
* SMPTE メタデータ レジストリ スプレッドシート メニュー。

### MXF 構造メタデータ

構造メタデータには、ファイルの内容に関する有用な情報が含まれているため、MXF ファイルの基本となります。 MXF メタデータには、フレーム レート、フレーム サイズ、ファイル作成日、カスタム変更日などの情報が含まれています。構造メタデータは、MXF ファイルの構造と機能を記述します。これには、さまざまな必須コンポーネントの技術的な記述と、出力タイムラインの構成方法の伝達が含まれます。

## 参考文献

* [MXF - ウィキペディア](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - プログレス レポート](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [MXF 用オープンソース C++ ライブラリ](http://www.freemxf.org/)

