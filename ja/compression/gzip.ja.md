{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZIP ファイル形式 - GNU Zip アーカイブ ファイル",
  "description":"GZIP ファイルとは何か,および GZIP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## .GZIP ファイルとは?

GZIP ファイルは、標準の [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) 圧縮アルゴリズムで作成された圧縮アーカイブです。圧縮されたアーカイブには、圧縮ファイル、ディレクトリ、ファイル スタブなど、複数のファイルが含まれる場合があります。ほとんどの Unix システムには、ファイルの圧縮/解凍用のオープン ソース gzip (GNU Zip) 圧縮ユーティリティが含まれています。 GZIP ファイルは、[WinZip](https://www.winzip.com/en/) などのアプリケーションで開くことができます。

## GZIP ファイル形式 - 詳細情報

GZIP は [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) アルゴリズムを使用して、ファイルをアーカイブに圧縮します。 [RFC1952](https://tools.ietf.org/html/rfc1952) と [RFC 1951](https://tools.ietf.org/html/rfc1951) の 2 つの RFC は、gzip ラッパー形式の仕様を定義しています。および圧縮データ形式をそれぞれ deflate します。

GZIP ファイルは、[GZ](/compression/gz/) ファイル形式で保存されることがよくあります。

## 参考文献

* [gzip](http://www.gzip.org/)
* [gzip - ウィキペディア](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP ファイル形式仕様](https://datatracker.ietf.org/doc/html/rfc1952)、IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

