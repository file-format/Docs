{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF ファイル形式と,NDF ファイルを作成して開くことができる API について学びます。",
  "title" :"NDF ファイル形式 - SQL Server マスター データベース ファイル",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .NDF オプション番号

拡張子が .ndf のファイルは、[Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) がユーザー データを格納するために使用するセカンダリ データベース ファイルです。 SQL サーバーはユーザー指定のデータを [MDF](/database/mdf/) と呼ばれるプライマリ ストレージ ファイルに格納するため、NDF はセカンダリ ストレージ ファイルです。 NDF データ ファイルはオプションであり、プライマリ MDF ファイルがすべての割り当てられたスペースを使用する場合にデータ ストレージを管理するためにユーザーが定義します。通常は別のディスクに保存され、複数のストレージ デバイスに分散する可能性があります。 NDF ファイルを開くには、MDF ファイルが存在する必要があります。

## NDF ファイル形式

NDF ファイル形式は [MDF](/database/mdf) と同じで、データ ストレージの基本単位としてページを使用します。各ページは、以下を含む 96 バイトのヘッダーで始まります。

* ページ ID
*構造の種類
* ページ内のレコード数
*前後のページへのポインター

### NDF ファイル構造

MDF ファイルのデータ構造は次のとおりです。

* ページ 0: ヘッダー
* ページ 1: 最初の PFS
* ページ 2: 最初の GAM
* 3 ページ: 最初の SGAM
※4ページ：未使用
※5ページ：未使用
* 6 ページ: 最初の DCM
* 7 ページ: 最初の BCM

#### NDF ファイル ヘッダー

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

## データファイルページ

SQL Server データ ファイル内のページはゼロ (0) から始まり、順次増加します。各ファイルは、一意のファイル ID 番号によって認識されます。ファイル ID とページ番号のペアは、データベース内のページを一意に識別します。データベースのページ番号を表示する例は、次の図のようになります。

{{< figure src="../ndf.png" alt="NDF データベース ファイル形式" >}}

この例は、4 MB のプライマリ データ ファイルと 1 MB のセカンダリ データ ファイルを持つデータベースのページ番号を示しています。

## 参考文献

* [データベース ファイルとファイル グループ](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [データベースのデタッチとアタッチ - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [SQL Server データ ファイルの分析](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

