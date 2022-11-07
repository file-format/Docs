---
date: 2019-10-11
keywords: prc,.prc,prc ファイル形式,prc ファイルの開き方,.prc 拡張子,prc 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC ファイル形式
linktitle: PRC
description: "PRC ファイル形式と,PRC ファイルを作成して開くことができる API について説明します。"
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC ファイル形式
「.prc」拡張子は、製品表現コンパクト 3D ファイル形式と MobiPocket による電子書籍ファイル形式に使用されています。

## Product Representation Compact (PRC) ファイルとは何ですか?

PRC (Product Representation Compact) は、特に CAD (コンピューター支援設計) システムからの 3D データを保存、読み込み、表示するために最適化された 3D ファイル形式です。これは、移植可能な方法で書かれたシーケンシャル バイナリ ファイルです。 PRC を使用して、3D データを PDF ファイルに埋め込むことができます。 PRC は、アセンブリとパーツ、3D エンティティのツリー、正確なジオメトリ表現、三角測量表現、マークアップなど、CAD の主な構成要素のほとんどをサポートしています。 PRC は .prc 拡張子を使用し、使用されるインターネット メディア タイプは *model/prc* です。

PRC は多目的ファイル形式で、用途に応じて通常の圧縮を使用して保存して CAD データを直接表現するか、高圧縮を使用して保存してファイル サイズを小さくすることができます。 PRC 形式を使用して PDF に保存された 3D データは、CAM および CAE アプリケーションと相互運用できます。

### Product Representation Compact (PRC) ファイル形式の仕様

PRC ファイルには、1 つのメイン ヘッダー セクションがあり、その後に 1 つ以上のファイル構造が続き、最後に 1 つのモデル ファイルが続きます。ファイル構造には、1 つのヘッダーとそれに続く次のデータ セクションがあります。

- **グローバル**: ファイル構造の各ツリー エンティティの参照ファイル構造と色、線種、および座標系が含まれます。
- **ツリー**: プロダクト オカレンス、パーツ定義、表現アイテム、マークアップなどのアイテムのツリーの説明が含まれています。
- **テッセレーション**: ツリーのリーフ エンティティ (表現アイテムとマークアップ) のすべてのテッセレーション (三角形化) データが含まれます。
- **ジオメトリ**: ツリーのリーフ エンティティ (表現アイテム) のすべての正確なジオメトリおよびトポロジ データが含まれます。
- **Extra geometry**: ジオメトリの概要データが含まれています。これにより、ジオメトリ全体をロードすることなく、ファイルを部分的にロードできます。

以下は、典型的な PRC ファイルの構造です。

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## PRC 拡張子を持つ MobiPocket 電子書籍ファイルとは
**Mobipocket** というフランスの会社によって導入された電子書籍ファイル形式も、拡張子 ".prc" を使用しています。 Mobipocket は当初、タブレット PC、PDA、スマートフォンなどの複数のスマート デバイス向けの無料アプリケーションをリリースしました。 「.prc」拡張子は、実際には .mobi と同じですが、特に **.prc** または **.pdb** 拡張子のみをサポートする PDA に使用されます。

### Mobipocket PRC ファイル形式の仕様
MobiPocket PRC ファイル形式は、XHTML を使用した Open eBook 標準に基づいており、JavaScript とフレームを含めることもできます。組み込みデータベースで使用されるネイティブ SQL クエリのサポートも利用できます。

Mobipocket Reader にはホームページ ライブラリがあります。読者は本の任意の部分に空白ページを挿入したり、可変図を追加したりできます。注釈、ブックマーク、修正、メモ、描画などのオブジェクトは、1 つの場所から管理できます。画像は GIF 形式に変換され、最大サイズは 64K で、画面の小さい携帯電話には十分です。 Mobipocket Reader には、電子ブックマークと組み込みの辞書があります。

リーダーには、多くの PDA、コミュニケーター、およびスマートフォンの読み取りとサポートのためのフルスクリーン モードがあります。 Mobipocket 製品は、ほとんどの Palm オペレーティング システム、Windows、Symbian、BlackBerry をサポートしていますが、Android はサポートしていません。リーダーは、WINE を使用して Linux または Mac OS X で動作します。

## 参考文献

- [中国 - ウィキペディア](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC フォーマット仕様](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [電子書籍フォーマットの比較 - ウィキペディアによる](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

