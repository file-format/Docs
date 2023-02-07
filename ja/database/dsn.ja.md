{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "DSN ファイルとは", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DSN ファイル形式と,DSN ファイルを作成して開くことができる API について学びます。",
  "title" :"DSNファイル形式 - データベースソース名ファイル",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## .DSN ファイルとは?

DSN は「Data Source Name」の略で、データベース接続情報を格納するために使用されるファイル形式です。 DSN ファイルは通常、ODBC (Open Database Connectivity) と組み合わせて使用され、サーバー名、ユーザー名、パスワードなどの接続に必要な情報を提供することで、特定のデータベースに簡単にアクセスできるようにします。通常、ファイルはプレーン テキストであり、テキスト エディタを使用して作成および編集できます。 Windows、Linux、Mac などのさまざまなオペレーティング システムで使用できます。

## DSNファイルを作成するには?

DSN ファイルの作成方法は、オペレーティング システムと使用可能なツールによって異なる場合があります。次の手順では、Windows システムで DSN ファイルを作成するプロセスの概要を説明します。

1. スタート メニューで「ODBC データ ソース」を検索して、ODBC データ ソース アドミニストレータを開きます。
2. [システム DSN] タブを選択し、[追加] ボタンをクリックします。
3. 接続するデータベースに適したドライバを選択し、[完了] をクリックします。
4. サーバー名、ユーザー名、パスワードなど、データベースに接続するために必要な情報を入力します。
5. [OK] をクリックして DSN ファイルを保存します。

または、拡張子が .dsn のプレーン テキスト ファイルを作成し、必要な接続情報を次の形式で入力して、手動で DSN ファイルを作成することもできます。

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

その後、このファイルのパスをコード/スクリプトで DSN として使用して、データベースに接続できます。

## DSNファイルを開くプログラム

DSN ファイルは、サーバー名、ユーザー名、パスワードなど、データベースへの接続に使用される情報を格納するプレーン テキスト ファイルです。通常、ODBC (Open Database Connectivity) と組み合わせて使用して、特定のデータベースに簡単にアクセスできるようにします。

DSN ファイルの内容を開いて表示するには、メモ帳、Sublime Text、Atom などの任意のテキスト エディターを使用できます。これらのプログラムを使用すると、DSN ファイルを開いて、そこに保存されている接続情報を表示できます。

ただし、DSN ファイルを使用してデータベースに接続し、SELECT、INSERT、UPDATE、DELETE などの操作を実行するには、Python、Java、C# などのプログラミング言語や Microsoft Access などのデータベース管理ツールなど、ODBC をサポートするプログラムが必要です。 、SQL Server Management Studio が必要です。これらのプログラムは、DSN ファイル内の情報を使用してデータベースに接続し、必要な操作を実行できます。

## 参考文献
* [DSN (データ ソース名) とは](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)
* [ODBC インポートのデータ ソースとして使用するファイル DSN を作成するにはどうすればよいですか?](https://www.ibm.com/support/pages/how-do-i-create-file-dsn-use-data-ソース-odbc-インポート)

