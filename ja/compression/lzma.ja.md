{
  "date" : "2021-04-08",
  "keywords" :[ "lzma ファイル", "lzma ファイル形式", "lzma ファイルとは", "ファイル", "lzma の例", "lzma ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA 圧縮ファイル形式",
  "description":"LZMA ファイルとは,LZMA ファイルを作成して開くことができる API です。",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## .LZMA オプション番号

拡張子が .lzma のファイルは、LZMA (Lempel-Ziv-Markov chain Algorithm) 圧縮方式を使用して作成された圧縮アーカイブ ファイルです。これらは主に Unix オペレーティング システムで検出/使用され、ファイル サイズを最小化するための [ZIP](/compression/zip/) などの他の圧縮アルゴリズムに似ています。 LZMA は従来のファイル形式であり、.xz 形式に置き換えられているか、置き換えられています。 .lzma 形式の MIME タイプは \`application/x-lzma' です。このファイル形式は、LZMA SDK で使用するために Igor Pavlov によって設計されました。

## LZMA ファイル形式

LZMA ファイルは、次の 2 つの主要部分で構成されています。

1.ヘッダー
1. 圧縮データ


### LZMAヘッダー

LZMA ファイルには 13 バイトのヘッダーがあり、その後に LZMA 圧縮データが続きます。 LZMA ヘッダーは次のもので構成されます。

* プロパティ
* 辞書サイズ
※未圧縮サイズ

#### LZMA ヘッダーのプロパティ

プロパティ フィールドには 3 つのプロパティが含まれています。略語は括弧内に示され、その後にプロパティの値の範囲が続きます。フィールドは以下で構成されます

1) リテラルコンテキストビットの数 (lc, [0, 8]);
2) リテラル位置ビットの数 (lp, [0, 4]);と
3) 位置ビットの数 (pb、[0、4])。

#### LZMA 辞書のサイズ

これは、2^n および 2^n + 2^(n-1) の範囲の値を持つ符号なし 32 ビットのリトル エンディアン整数として格納されます。 LZMA Utils は、任意の辞書サイズのファイルを解凍できます。

#### 非圧縮サイズ
Uncompressed Size は、符号なし 64 ビットのリトル エンディアン整数として格納されます。 0xFFFF_FFFF_FFFF_FFFF という特殊な値は、非圧縮サイズが不明であることを示します。 Uncompressed Size が不明な場合に限り、値は End of Payload Marker (\*) で表されます。

## 参考文献

* [Lempel–Ziv–Markov 連鎖アルゴリズム](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
