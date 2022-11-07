{
  "date" : "2019-12-09",
  "keywords" :[ "zl ファイル", "zl ファイル形式", "zl ファイルとは", "ファイル", "zl の例", "zl ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP 圧縮ファイル形式",
  "description":"ZL ファイル形式と,ZL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## .ZL オプション番号

拡張子が .zl のファイルは、ファイルの圧縮に DEFLATE 圧縮アルゴリズムの変形を使用する ZLIP 圧縮ファイル形式です。これは、CPU タイプ、オペレーティング システム、ファイル システム、および文字セットに依存しないため、情報の交換に使用できます。 ZLIP 圧縮の技術仕様は [IETF サイト](https://tools.ietf.org/html/rfc1950) で公開されており、開発者の観点から参照できます。

## ZL ファイル形式

zlib ストリームの構造は次のとおりです。

* `CMF (Compression Method and flags)` - このバイトは、圧縮方法に応じて 4 ビットの圧縮方法と 4 ビットの情報フィールドに分割されます。
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (圧縮方法)` - ファイルで使用されている圧縮方法を識別します。その値と対応する圧縮方法は次のとおりです。

| | CM値|圧縮|
|---|---|
|CM = 8|最大 32K のウィンドウ サイズでの DEFLATE|
|CM = 15|予約済み|

* `CINFO (圧縮情報)` - CM = 8 の場合、CINFO は LZ77 ウィンドウ サイズの 2 を底とする対数から 8 を引いたものです (CINFO=7 は 32K ウィンドウ サイズを示します)。

* `FLG (FLaGs)` - このフラグ バイトは次のように分割されます。
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## 参照 ##

※【Zlibファイル形式仕様】(https://tools.ietf.org/html/rfc1950)

