{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - レポート定義言語クライアント側",
  "keywords" :["rdlc","レポート定義言語","mkv形式","XSD","レポート定義言語クライアント側"],
  "description":"SQL Server Reporting Services レポート定義の XML 表現である RDLC ファイル形式について学びます。",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## .RDLC オプション番号##

RDLC は Report Definition Language Client side の略です。実際には、Microsoft レポート テクノロジを使用して作成されたレポート ファイルの拡張子です。これらのファイルの作成には、レポート デザイナーの SQL Server 2005 バージョンが使用されます。クライアント側の **ReportViewer** コントロールは、RDLC レポートを直接実行できます。

## RDL ファイルと RDLC ファイル
|.rdl ファイル |.rdlc ファイル|
---|---|
|RDL ファイルは、レポート デザイナーの SQL Server 2005 バージョンによって作成されます|RDLC ファイルは、レポート デザイナーの Visual Studio 2005 バージョンによって作成されます|
|SQL Server Reporting Services で使用されます|Visual Studio で使用されます|
|リモートレポートです|ローカルレポートです|
|それを実行するには、Reporting Services インスタンスが必要です|Reporting Services インスタンスは必要ありません|

## クライアント レポート定義 (.rdlc) ファイルの作成
ReportViewer コントロールは、コントロールの組み込み処理機能を使用してクライアント レポート定義 (.rdlc) ファイルを実行するために使用されます。ローカル処理モードで実行するクライアント レポートは、アプリケーション プロジェクトで簡単に作成できます。レポートを作成する方法は次のとおりです。

- **レポート ウィザード**を使用して、新しいクライアント レポート定義 (.rdlc) を作成します。

- Visual Studio を使用して、新しいクライアント レポート定義 (.rdlc) ファイルを作成します。

- レポート定義をプログラムで生成します。


**ReportViewer** コントロールでレポートを実行することによってのみ、レポートをプレビューできます。いつでもレポート定義を開いて編集し、アプリケーションをビルドまたはデプロイして結果を確認できることに注意してください。

## 参照 ##

- [クライアント レポート定義 (.rdlc) ファイルの作成](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

