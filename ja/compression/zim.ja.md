{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM ファイル形式 - OpenZIM アーカイブ ファイル",
  "description":"ZIM ファイル形式と,ZIM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## .ZIM オプション番号##

拡張子が .zim のファイルは、Wiki コンテンツをオフラインで保存するために作成されたアーカイブです。ウィキペディアを USB に保存するのに最も適したオープン ファイル形式と考えられています。サイトのコンテンツをコンパクトな形式で保存します。その名前は、以前の Zeno ファイル形式であった "Zeno IMproved" に由来します。 ZIM は [openZIM ](https://openzim.org/) プロジェクトによって維持されています。このプロジェクトはウィキメディア CH が後援し、ウィキメディア財団が支援しています。 ZIM ファイルは、Kiwix や ZIMReader などのアプリケーションで開くことができます。 OpenZIM プロジェクトは、OpenSource コミュニティからの貢献のために [Github](https://github.com/openzim) で ZIM ファイル形式の実装をホストしています。

## ZIM ファイル形式の仕様

ZIM ファイル形式は、[Zeno ファイル形式](https://openzim.org/wiki/Zeno_file_format) の上に開発されたもので、後方互換性はありません。 ZIM ファイル形式の形式仕様は、[オンラインで入手可能](https://openzim.org/wiki/ZIM_file_format) で、開発者の参照用に openZIM によって公開されています。 OpenZIM は、ZIM ファイルを読み書きするための C++ オープン ソース実装 [LibZim](https://openzim.org/wiki/Zimlib) を提供しています。

ZIM ファイル形式は、コンテンツをコンパクトにするために LZMA2 圧縮を使用します。

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM ファイル形式" >}}


### ZIMヘッダー

ZIM ファイルは、オフセット 0 のヘッダーで始まります。すべての構成要素はリトル エンディアンに基づいており、すべての整数は符号なし整数 (uint_16、uint_32、uint_64) です。

|フィールド名 |タイプ|オフセット|長さ|説明|
---|---|---|---|---|
|マジックナンバー|整数| 0| 4|ファイル形式を認識するためのマジック ナンバーは、72173914 (0x44D495A) でなければなりません。
|メジャーバージョン|整数| 4| 2| ZIM ファイル形式のメジャー バージョン (5 または 6)|
|マイナーバージョン|整数| 6| 2| ZIM ファイル形式のマイナー バージョン|
|uuid|整数| 8| 16|この zim ファイルの一意の ID|
|記事数|整数| 24| 4|記事の総数|
|クラスター数|整数| 28| 4|クラスターの総数|
|urlPtrPos|整数| 32| 8| URL 順のディレクトリ ポインタ リストの位置 |
|titlePtrPos|整数| 40| 8|タイトルによって並べ替えられたディレクトリ ポインタ リストの位置|
|clusterPtrPos|整数| 48| 8|クラスタ ポインタ リストの位置 |
|mimeListPos|整数| 56| 8| MIME タイプ リストの位置 (ヘッダー サイズも) |
|メインページ|整数| 64| 4|メインページまたはメインページがない場合は 0xffffffff|
|レイアウトページ|整数| 68| 4|レイアウト ページまたはレイアウト ページがない場合は 0xffffffffff|
|チェックサム位置|整数| 72| 8|チェックサム自体を含まない、このファイルの md5checksum へのポインター。これは、常にファイルの末尾の 16 バイト前を指します。|

## 参照 ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

