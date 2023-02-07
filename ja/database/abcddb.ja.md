{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "ABCDDB ファイルとは", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ABCDDB ファイル形式と,ABCDDB ファイルを作成して開くことができる API について学びます。",
  "title" :"ABCDDB ファイル形式 - Apple アドレス帳連絡先リスト データベース ファイル",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## ABCDDB ファイルとは?

拡張子が **.ABCDDB** のファイルは、Apple Address Book Contact List Database を表します。これは、一般に **Contacts** としても知られる **Address Book** アプリケーションに属します。これは組み込みアプリケーションであり、iOS および macOS オペレーティング システムに含まれています。連絡先アプリケーションを使用すると、ユーザーは個人、企業、組織などの連絡先に関連する情報を保存および整理できます。このアプリを使用すると、ユーザーは名前、住所、電話番号、メール アドレスなどの詳細を追跡したり、連絡先をグループに分類したりできます。

## SQLite との関係と典型的なパス

Apple の AddressBook (Contacts とも呼ばれます) は、連絡先情報を vCard としてメタデータ フォルダーに保存します。 **ファイル _ABCDDB_ は、実際には _SQLite 3 データファイル_** です。

SQLite は、軽量で自己完結型になるように設計された一般的なデータベース管理システムです。さまざまな種類のソフトウェアやデバイスで使用されています。 SQLite は RDBMS の一種で、キーによって相互に関連付けられたテーブルにデータを格納します。整数、浮動小数点数、文字列、バイナリ データなど、さまざまなデータ型を処理できます。さらに、SQLite はトランザクションをサポートしているため、ユーザーは複数のデータベース操作を 1 つの作業単位として一緒に実行できます。

ABCDDB 拡張子を持つファイルは通常、ここに保存されます

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## 破損した連絡先データベースの修正

これを行う前に、まずバックアップを取ってください。次に、に移動してください

`~/Library/Application Support/AddressBook`

そのディレクトリには、拡張子が .abcddb のものを含む 3 つのファイルがあります。

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

これらのファイルをすべて削除し、連絡先を再度開くと、再び機能し始めます。

## バックアップから AddressBook データベースを復元する

AddressBook データベースの連絡先が「addressbook-v22.abcddb」に保存されているとします。

- 最初にアドレスブック データをバックアップし、すべてのアプリケーションを終了します。
- データベース ファイルを `~/Library/Application Support/AddressBook` サブディレクトリに移動します
- **Address Book.app** を起動します。

## ABCDDB ファイル データを Microsoft Access にエクスポートする

ファイルは SQLite 3 データファイルなので、ODBC コネクタを使用して abcddb ファイル内のデータを Microsoft Access にエクスポートできます。

SQLite ODBC コネクタは、ODBC インターフェイスをサポートするアプリケーションが SQLite データベースに接続できるようにするソフトウェア ライブラリおよびドライバです。これには、ODBC インターフェイスを定義するライブラリと、このインターフェイスを SQLite API の呼び出しに変換するドライバーが含まれています。 SQLite ODBC コネクタを利用するには、まずコネクタをインストールしてから、コンピュータに ODBC データ ソースを設定する必要があります。これらの手順を完了すると、ODBC サポートを備えたすべてのアプリケーションがデータ ソースに接続し、SQLite データベースからデータを取得できるようになります。

## 参考文献
* [破損した連絡先データベースを修正](https://discussions.apple.com/docs/DOC-10581)
* [Mac用連絡先データベース](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [Windows 7 Excel で abcddb ファイルを開く、またはエクスポートするにはどうすればよいですか?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file- in-windows-7-excel)

