{
  "date" : "2022-01-23",
  "keywords" :[ "xz ファイル", "ファイル形式", "xz ファイルとは", "ファイル", "xz 例", "xz ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ ファイル - XZ 圧縮アーカイブ",
  "description":"XZ ファイル形式と,XZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## .XZ オプション番号

XZ は、LZMA2 圧縮アルゴリズムを利用する圧縮ファイル形式です。これは、一般的な gzip および bzip2 形式の代替として設計されており、これらの古い標準よりも多くの利点があります。 XZ ファイルは、多くのプラットフォームで十分にサポートされており、すばやく簡単に解凍できます。 [ZIP](/compression/zip/) や [RAR](/compression/rar/) ファイルほど一般的ではありませんが、XZ アーカイブを使用して、圧縮品質を犠牲にすることなく大量のデータを保存できます。大きなファイルを圧縮または解凍する必要がある場合は、XZ ファイル拡張子を検討する価値があります。

## XZ ファイル形式

XZ ファイルが生成され、バイナリ ファイルとしてディスクに保存されます。 LZMA アルゴリズムを使用してデータを圧縮し、最大 50% の圧縮率を達成できます。 XZ ファイルは通常、ソフトウェアの配布とバックアップ アーカイブに使用されます。それらは、ほとんどの Linux ディストリビューションに含まれている XZ ユーティリティを使用して解凍できます。

## Linux/Unix で XZ ファイルを解凍する

XZ ファイルを解凍するには、最初に「xz-utils」パッケージをインストールします。
```
$ sudo apt-get install xz-utils
```

「unxz」コマンドを使用して、.xz ファイルを抽出します。
```
$ unxz compressed_xz_file.xz
```

または XZ の --decompress オプションで使用:
```
$ xz --decompress compressed_xz_file.xz
```

## 参考文献

* [XZ ユーティリティ](https://en.wikipedia.org/wiki/XZ_Utils)

