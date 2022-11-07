---
date: 2019-12-09
keywords: arc,.arc,arc ファイル形式,arc ファイルの開き方,.arc 拡張子,arc 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC ファイル形式
linktitle: ARC
description: "ARC ファイル形式と,ARC ファイルを作成して開くことができる API について学習します。"
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## .ARC ファイルとは何ですか?

ARC は、System Enhancement Associates (SEA) によって開発されたロスレス データ圧縮およびアーカイブ形式です。ファイル形式とそれを作成するアプリケーションは両方とも ARC と呼ばれます。 ARC は、圧縮機能と複数のファイルを同じファイルにアーカイブする機能を組み合わせた、ダイヤルアップ BBS の初期の頃に非常に人気がありました。 ARC は後に、より優れた圧縮率を提供する [ZIP](/compression/zip/) に置き換えられました。

.arc ファイル拡張子は、インターネット アーカイブが複数の Web リソースを保存するために使用する ARC 形式、FreeArc アーカイバが使用する別の ARC 形式、任天堂がリソースに使用する別の形式など、関連のない他のいくつかのアーカイブ ファイル タイプで使用されます。 .

## ARC ファイル形式の歴史

ARC プログラムは、1985 年に System Enhancement Associates の Thom Henderson によって作成されました。このプログラムは、ファイルを 1 つのアーカイブ ファイルにグループ化し、圧縮も行いました。 ARC プログラムによって生成されたファイルには、.arc 拡張子が使用されていました。 SEA は 1986 年に ARC のソース コードをリリースし、ARC は 1987 年に Howard Chu によって Unix と Atari ST に移植されました。

Phil Katz は、ファイルをアーカイブおよび抽出するための PKARC および PKXARC を開発しました。ファイルは ARC ファイル形式で動作し、大幅に高速でした。 ARC とは異なり、Katz は圧縮機能とアーカイブ機能を 2 つの異なるファイルに分割し、実行に必要なメモリを削減しました。

SEA と Katz の間の訴訟の後、SEA はシェアウェア市場から撤退し、フルスクリーンのユーザー インターフェイスを備えた ARC+Plus を開発しました。 ARC 形式は PC では一般的ではなくなりました。

## ARC ファイル形式

ARC ファイルは、以下に示すように、一連のファイル ヘッダーとファイル、その後に続くアーカイブ終了マーカーで構成されます。

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC ファイルのヘッダー ###

|オフセット|ラベル|タイプ|値|説明|
|---|---|---|---|---|
|00|ARCID |DB|$1A| | |
|01|ARCMTD|DB|00|メソッド|
|02|ARCFNT|DS|12|ファイル名|
|0E| |DB|00| | |
|0F|ARCNSZ|HEX|00000000|圧縮サイズ|
|13|ARCDAT|DW|0000|ファイルの日付 (MSDOS)|
|15|ARCTIM|DW|0000|ファイル時間 (MSDOS)|
|17|ARCCRC|DW|0000| | |
|19|ARCOSZ|HEX|00000000|非圧縮サイズ|
|1D|ARCFIL|DS|ARCNSZ| | |

### 圧縮方法 ###

圧縮方法バイトは、使用される圧縮方法を示します。以下は、ARC ファイルに使用される圧縮方法です。

|メソッド|名前|説明|
|---|---|---|
|0|保存|圧縮なし|
|1|Packed|反復ランニングレングスエンコーディング (RLE)|
|2|スクイーズド|ハフマン符号化|
|3|Crunched|4K バッファー、12 ビット コードの LZW|
|4|Crunched|最初にパッキングし、次に 12 ビットの LZW 4K バッファ|
|5|クランチ|パッキング、LZW、4K バッファ、可変長 (9 ～ 12 ビット)|
|6|Squashed|LZW、8K バッファー、可変長 (9 ～ 13 ビット)|
|7|クラッシュ|パッキング、その後 LZW 8K バッファ、2 ～ 13 ビット (PAK 1.0)|
|8|蒸留|8K バッファ (PAK 2.0) を使用したダイナミック ハフマン|

## 参考文献

- [ARC (ファイル形式) - ウィキペディア](https://en.wikipedia.org/wiki/ARC_(file_format))

