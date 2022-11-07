---
date: 2022-03-20
keywords: mxl,Musepack ファイル形式,.mxl 拡張子
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "MXL ファイル形式と,MXL ファイルを作成して開くことができる API について学びます。"
title: MXL ファイル形式 - 圧縮された MusicXML ファイル
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## .MXL オプション番号

MXL ファイルは、デジタル楽譜を交換するためのオープン スタンダード フォーマットである MusicXML ファイル フォーマットの圧縮形式です。プレーン テキストの MusicXML ファイルはサイズが大きく、このようなファイルをシート配布形式として使用すると、ファイル サイズが大きくなって影響を受けました。この問題は、[MusicXML](https://www.musicxml.com/) 2.0 で、ファイルを十分に圧縮して元の MIDI ファイルと同様にファイル サイズを小さくする MXL ファイル形式を導入することで処理されました。 MXL ファイルの推奨メディア タイプは、application/vnd.recordare.musicxml です。

## MXL ファイル形式

MXL ファイルは、.mxl ファイル拡張子を持つ [ZIP](/compression/zip/) 圧縮された [XML](/web/xml/) ファイルとして保存されます。 MXL ファイルは、[RFC 1951](https://www.ietf.org/rfc/rfc1951.txt) で指定されているように、DEFLATE アルゴリズムで圧縮されます。

### MXL ファイル構造

各 MXL ファイルには、ファイルの MusicXML バージョンの開始点を記述する META-INF/container.xml ファイルが必要な ZIP ベースの XML 形式があります。 MXL ファイル形式に対応する .xsd ファイルは定義されていません。

シンプルな container.xml ファイルの内容は次のとおりです。この例は、MakeMusic Web サイトで入手できる Dichterliebe01.mxl ファイルから取得したものです。

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
この例では、<container> element はドキュメント要素です。の<rootfiles>要素には 1 つ以上を含めることができます<rootfile>要素、最初の<rootfile>MusicXML ルートを記述する要素。として使用される MusicXML ファイル<rootfile>がある可能性があり<score-partwise>、<score-timewise> 、 また<opus>ドキュメント要素として。

## 参考文献

※【圧縮MXLファイル】(https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

