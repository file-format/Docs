{
  "date" : "2019-10-11",
  "keywords" :["wmzファイル","wmzファイル形式","wmzファイルとは","ファイル","wmz例","wmzファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ ファイル形式 - 圧縮された Windows メタファイル",
  "description":"WMZ ファイル形式と,WMZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## .WMZ オプション番号

拡張子が .wmz のファイルは、[WMF](/image/wmf/) の圧縮バージョンであり、メタファイルの保存に使用されます。これは、古いバージョンの Microsoft Office アプリケーションによって生成される中間レベルのファイルであり、あまり一般的に使用されていません。 WMZ ファイルは、ドキュメントを [HTML](/web/html/) 形式で保存するときに生成されます。これらは、埋め込まれたクリップ アートや数式などを含むドキュメントを電子メールで送信する際にも生成される可能性があります。WMZ ファイルを開くことができるアプリケーションには、Corel Winzip および Apple Archive Utility が含まれます (ただし、これらに限定されません)。

## WMZ ファイル形式

WMZ ファイルは [Gzip](/compression/gz/) 圧縮されており、内部に [WMF](/image/WMF/) が含まれています。 Gzip は、アーカイブの圧縮に DEFLATE アルゴリズムを使用します。 GZIP は [ZIP](/compression/zip/) アーカイブ形式とは異なります。圧縮アルゴリズムを個々のファイルではなく完全なアーカイブに適用するためです。ファイル形式は次のもので構成されます。

* ファイルヘッダー
* オプションのヘッダー
* 圧縮データ
* ファイルフッター

Internet Engineering Task Force (IETF) によって発行された GZIP ファイル形式 [仕様バージョン 4.3](http://tools.ietf.org/html/rfc1952) には、ファイル形式に関する詳細な情報が含まれています。

## 参考文献

* [RFC1952: GZIP ファイル形式仕様](http://tools.ietf.org/html/rfc1952)、[IETF](https://ietf.org) による
* [Windows メタファイル - ウィキペディア](https://en.wikipedia.org/wiki/Windows_Metafile)

