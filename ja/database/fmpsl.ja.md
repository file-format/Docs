{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FMPSL ファイル形式と,FMPSL ファイルを作成して開くことができる API について学びます。",
  "title" :"FMPSL ファイル形式 - FileMaker Pro 12 スナップショット リンク ファイル",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## .FMPSファイルとは?

FMPSL ファイルは、FileMaker Pro 12 で作成されたデータベースのスナップショット ファイルです。このファイルには、データベースからクエリされた結果が、視覚的なレイアウトや表示情報などの他の情報とともに保存されます。 FMPSL ファイルを使用して、このすべてのデータを FileMaker Pro データベースの別のインスタンスに復元できます。このファイル形式は、FileMaker Pro v 12 の起動とともに導入されました。このバージョンより前のバージョンでは、スナップショット リンクは FileMaker Pro v 11 で FPSL ファイル形式として導入されました。FMPSL ファイルは FileMaker Pro Advanced ソフトウェアで開くことができます。 FileMaker Pro でサポートされているその他のファイル形式には、[FP5](/database/fp5/)、[FP7](/database/fp7/)、および [FMP12](/database/fmp12/) があります。

## FMPSL ファイル形式

FMPSL ファイルの内部ファイル形式の詳細は、開発者の参照用に公開されていません。

### レコードを FMPSL ファイルとして保存するには?

FileMaker Pro データベースのデータは、次の手順を使用してスナップショット リンク ファイルとして保存できます。

1. スナップショット リンク ファイルとして保存する必要があるデータベースからレコードを検索します。
1. メニューから [Send Record As Snapshot Link] オプションを使用して、ファイル名を入力してファイルを保存します。
1. 参照中のレコードを使用して、見つかったレコード セット全体を保存します。

生成されたスナップショット ファイルは、指定した名前でディスクに保存されます。

## 参考文献

* [以前のバージョンの FileMaker Pro ファイル形式を FMP12 ファイル形式に変換](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [レコードをスナップショット リンク ファイルとして保存](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)
