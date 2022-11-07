{
  "date" : "2019-10-11",
  "keywords" :[ "bz2 ファイル", "bz2 ファイル形式", "bz2 ファイルとは", "ファイル", "bz2 の例", "bz2 ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - 圧縮ファイル形式",
  "description":"BZ2 ファイルとは何か,BZ2 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## .BZ2 ファイルとは何ですか?

BZ2 は、[BZIP2](http://www.bzip.org/) オープン ソースの圧縮方法を使用して生成された圧縮ファイルで、主に UNIX または Linux システムで使用されます。単一のファイルの圧縮に使用され、複数のファイルのアーカイブには使用されません。これは、複数のファイルを圧縮せずに 1 つのファイルにアーカイブする同じプラットフォームの TAR ファイル形式とは対照的です。 BZ2 で圧縮されたファイルは、[WinZip](https://www.winzip.com/win/en/) などのアプリケーションで解凍できます。 BZIP2 は、Run-Length Encoding (RLE) または [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) 圧縮アルゴリズムを使用して、高レベルの圧縮を実現します。

## BZ2 ファイル形式

このファイル形式に使用できる正式な仕様はありません。ただし、非公式の [リバース エンジニアリングされた仕様](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) は、.bz2 ストリームが 4 バイトのヘッダーで構成され、その後に続くことを示しています。 0 個以上の圧縮ブロックによって。その直後に、処理されたプレーン テキストのストリーム全体の 32 ビット CRC を含むストリーム終了マーカーが続きます。圧縮されたブロック間にパディングはなく、すべてのブロックがビット整列されます。

## BZ2 ファイルの解凍/解凍

WinZip などのソフトウェアを使用して、Windows および Mac OS で BZ2 ファイルを解凍できます。 Linux では、ターミナルで次のコマンドを実行します。

```
bzip2 -d filename.bz2
```

## 参考文献

※【BZIP2フォーマット仕様書】(https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

