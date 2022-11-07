{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir レポート テンプレート ファイル",
  "description":"RML ファイルと,RML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## .RML オプション番号

RML ファイルは、[Elixir Repertoire](https://elixirtech.com/repertoire-2/) レポート エンジンを使用したレポート テンプレート ファイルです。テンプレート ファイルは、データ ソースが Elixir FileSystem に接続されたレポートを生成するために使用されます。データは読み取られ、RML テンプレート ファイルに取り込まれ、[PDF](/pdf/)、[RTF](/word-processing/rtf/)、スプレッドシート [XLS] などのさまざまなファイル形式にエクスポートできます。 (/スプレッドシート/xls/)。 Elixir Repertoire レポート エンジンは、さまざまな JDBC データ ソースに接続できます。

## RML ファイル形式

RML ファイル形式の内部ファイル構造の詳細は公開されていません。ファイルは Elixir Repertoire アプリケーションによって内部的に生成および保存され、接続されたデータ ソースから取り込まれたデータを含むレポートを生成します。 RML テンプレート ファイルには、データから生成される最終レポートの全体的なレイアウトとプレースホルダー情報が含まれています。

## RML テンプレート ファイルの作成方法

Elixir Repertoire で RML テンプレートを生成するには、次の手順に従います。

1. JDBC データ ソースをファイル システムに接続します。
1. レポート テンプレート ウィザードの起動
1. ソフトウェアを使用して、データソース .ds ファイルを見つけます。
1.エクスポートの選択肢として表形式のレポートを選択します
1. レポート テンプレートに含めるフィールドを選択します
1. 最後に、[完了] ボタンをクリックすると、最初の report.rml がリポジトリに追加され、開かれて [レイアウト] タブが表示されます。

## 参考文献

* [エリクサーレパートリー](https://elixirtech.com/repertoire-2/)

