---
date: 2020-08-12
keywords: jfif,.jfif,jfif ファイル形式,jfif ファイルの開き方,.jfif 拡張子,jfif 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF ファイル - .jfif ファイルとは?
linktitle: JFIF
description: "JFIF ファイル形式と,JFIF ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## .JFIF ファイルとは何ですか?

JFIF (JPEG File Interchange Format (JFIF)) は、.jfif 拡張子を使用する画像形式ファイルです。 JFIF は、複雑さを軽減し、その制限を解決することにより、JIF (JPEG Interchange Format) を基に構築されています。

## JFIFの歴史

JFIF 文書の開発は Eric Hamilton が主導し、最初のバージョンに関する合意が 1991 年後半に確立されました。バージョン 1.02 は 1992 年 9 月 7 日に公開されました。 JFIF は 2009 年に ECMA によって発行され、2011 年に ITU-T によってその勧告 T.871 として標準化され、2013 年に ISO/IEC によって ISO/IEC 10918-5 として標準化されました。

## JFIF ファイル形式 ##

JFIF ファイルは、JPEG 規格のパート 1 で定義されている一連のマーカーで構成されています。各マーカーは 2 バイト (FF の後にマーカーのタイプを指定するバイトが続く) で構成されます。マーカーは、スタンドアロンにすることも、マーカー セグメントの開始を示すこともできます。

JFIF では、Y、Cb、Cr などの複数のコンポーネントを異なる解像度にすることができますが、それらの配置は定義されていません。 JPEG とは異なり、JFIF は解像度と縦横比の情報を提供できます。 JFIF は、使用するカラー モデルも定義します。

### ファイル構造 ##

|セグメント|コード|説明|
|---|---|---|
|SOI|FF D8|画像の開始|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|追加のマーカー セグメント|
|SOS|FF DA|スキャン開始|
||圧縮画像データ||
|EOI|FF D9|画像の終わり|

JFIF 標準では、次のセグメントが定義されています。

### JFIF APP0 マーカー セグメント ###

これは、イメージ パラメータを含む必須のセグメントです。非圧縮のサムネイルを埋め込むこともできます。

|フィールド|サイズ (バイト)|説明|
|---|---|---|
|APP0マーカー|2|FF E0|
|長さ|2|APP0 マーカーを除くセグメントの長さ|
|識別子|5|NULL バイトで終了する ASCII の JFIF (4A 46 49 46 00)|
|JFIF バージョン|2|JFIF のバージョン|
|密度単位|1|次のピクセル密度フィールドの単位</br>00 : 単位なし。 width:height ピクセルの縦横比は Ydensity:Xdensity に等しい</br>01 : 1 インチあたりのピクセル数</br>02 : ピクセル/センチメートル|
|Xdensity|2|ゼロより大きい水平ピクセル密度|
|Ydensity|2|ゼロより大きい垂直ピクセル密度|
|Xthumbnail|1|埋め込まれた RGB サムネイルの水平ピクセル数。ゼロかもしれません|
|Ythumbnail|1|埋め込まれた RGB サムネイルの垂直方向のピクセル数。ゼロかもしれません|
|サムネイルデータ|3×n|非圧縮24ビットRGBラスターサムネイルデータ|

### JFIF 拡張 APP0 マーカー セグメント ###

これはオプションのセクションであり、定義されている場合、JFIF APP0 マーカー セグメントの直後に続く必要があります。このセクションは、JFIF バージョン 1.02 以降でサポートされており、3 つの異なる形式でサムネイルを埋め込むことができます。

|フィールド|サイズ (バイト)|説明|
|---|---|---|
|APP0マーカー|2|FF E0|
|長さ|2|APP0マーカーを除くセグメントの長さ|
|識別子|5|NULL バイトで終了する ASCII の JFXX (4A 46 58 58 00)|
|サムネイル形式|1|次の埋め込みサムネイルに使用するデータ形式を指定します:</br> 10 : JPEG形式</br>11 : 1 ピクセルあたり 1 バイトのパレット形式</br>13 : ピクセルごとに 3 バイトの RGB フォーマット|
|サムネイルデータ|変数||

## JFIFから他の画像ファイル形式への変換

JFIF は、[PNG](/image/png/)、[JPG](/image/jpg/)、[PDF](/pdf/) などの一般的な画像ファイル形式に変換できます。

## 参照 ##

- [JFIF - ウィキペディア](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)
