{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "Btrieve データベース" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BTR ファイル形式と,BTR ファイルを作成して開くことができる API について学びます。",
  "title" :"BTR - Btrieve データベース ファイル",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## .BTR オプション番号

拡張子が .btr のファイルは、[Btrieve](https://www.actian.com/) トランザクション データベース アプリケーションによって作成されたデータベース ファイルです。リレーショナル データベース管理システム (RBMS) とは異なり、Btrieve は Indexed Sequential Access Method (ISAM) に基づいています。これは、高速検索のためにデータを格納する方法です。 BTR ファイルにはレコードのコレクションが保存され、要件に従ってレポートを生成するために使用されます。 BTR ファイルは、Pervasive Btrieve Database Manager、Pervasive PSQL Maintenance Utility、および Legend Software BTRIEVE Viewer を使用して開くことができます。

## BTR ファイル構造 - 詳細情報

BTR ファイルの構造内の各バイトの内部データ構造とアライメントは公開されていません。ただし、Btrieve
BTR ファイルから情報を読み取るために使用できる [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) を提供します。以下のプログラミング言語と開発環境に対応しています。

* エンバカデロ C/C++
* エンバカデロ デルフィ
* GNU C/C++
* マイクロ フォーカス COBOL
*マイクロソフトビジュアルベーシック
* マイクロソフト ビジュアル C++
* ワトコム C/C++

BTR ファイルからのデータの取得は、関連する DDF ファイルに依存します。 DDF がなければ、そのようなファイルから情報を取得するのは簡単ではありません。

## 参考文献

* [Btrieve - ウィキペディア](https://en.wikipedia.org/wiki/Btrieve)
* [Btreive API の紹介](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

