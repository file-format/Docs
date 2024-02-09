{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF ファイル形式と,MDF ファイルを作成して開くことができる API について学びます。",
  "title" :"MDF ファイル形式 - SQL Server マスター データベース ファイル",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .MDF オプション番号

拡張子が .mdf のファイルは、[Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) がユーザー データを保存するために使用するマスター データベース ファイルです。すべてのデータがこのファイルに保存されるため、これは非常に重要です。 MDF ファイルは、フォームの列、行、フィールド、インデックス、ビュー、およびテーブルのリレーショナル データベースにユーザー データを格納します。 SQL Server では、autogrow と autoshrink の設定を設定して、データベースのパフォーマンスにプラスの影響を与えることができます。 MDF ファイルは、Microsoft SQL Server を使用してデータベースにロードおよびアタッチできます。 MDF ファイルには Application/octet-stream MIME タイプがあります。

## MDF ファイル形式

SQL Server のデータ ストレージの基本単位はページです。データベースに割り当てられたストレージ ページは、0 から n までの番号が付けられた論理ページに分割されます。 1 つのページは、ページ ID、ページが属する構造のタイプ、ページ内のレコード数、および前後のページへのポインターで構成される 96 バイトのヘッダーで始まります。

### ファイル構造

MDF ファイルのデータ構造は次のとおりです。

* ページ 0: ヘッダー
* ページ 1: 最初の PFS
* ページ 2: 最初の GAM
* 3 ページ: 最初の SGAM
※4ページ：未使用
※5ページ：未使用
* 6 ページ: 最初の DCM
* 7 ページ: 最初の BCM

#### ファイル ヘッダー

すべてのファイルのページ番号 0 には、ファイルに関するメタデータを格納するヘッダーが含まれています。

#### ページの空き領域 (PFS)
PFS は割り当てステータスを識別し、空き領域の量を決定します。

* ビット 1: ページが割り当てられているかどうかを示します。
* ビット 2: ページが混合エクステントからのものかどうかを示します。
* ビット 3: このページが IAM ページであることを示します。
* ビット 4: このページにゴースト レコードが含まれていることを示します
* ビット 5 から 7: 次のようにページの充足度を示す結合された 3 ビット値:
* 0: ページは空です
* 1: ページは 1 ～ 50% 埋まっています
* 2: ページは 51 ～ 80% 埋まっています
* 3: ページは 81 ～ 95% 埋まっています
* 4: ページは 96 ～ 100% 埋まっています

## 参考文献

* [データベース ファイルとファイル グループ](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [データベースのデタッチとアタッチ - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [SQL Server データ ファイルの分析](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

