{
  "date" : "2019-10-11",
  "keywords" :[ "tbz ファイル", "tbz ファイル形式", "tbz ファイルとは", "ファイル", "tbz の例", "tbz ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip圧縮タールアーカイブ",
  "description":"TBZ ファイル形式と,TBZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## .TBZ オプション番号

拡張子が .tbz のファイルは、コンテンツ ファイルのサイズを縮小するために BZIP 圧縮を使用する圧縮アーカイブです。 TBZ ファイルは、実際には BZIP で圧縮された UNIX [TAR](/compression/tar/) アーカイブ ファイルです。最新の第 2 レベルの圧縮は [BZIP2](/compression/bz2/) で、BZIP に取って代わりました。 TBZ ファイル形式は、大きなファイルの転送に適しています。 TBZ ファイルは、7-Zip、PeaZip、jZip などのソフトウェア アプリケーションを使用して開いたり抽出したりできます。 Linux および macOS ユーザーは、ターミナル ウィンドウから BZIP2 コマンドを使用して TBZ を開くこともできます。

## TBZ ファイル形式

TBZ ファイルは、実際には BZIP/[BZIP2](/compression/bz2) 圧縮で作成された圧縮アーカイブです。このファイル形式に使用できる正式な仕様はありません。ただし、非公式の [リバース エンジニアリングされた仕様](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) は、.bz2 ストリームが 4 バイトのヘッダーで構成され、その後に続くことを示しています。 0 個以上の圧縮ブロックによって。

## 参照 ##

※【BZIP2フォーマット仕様書】(https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

