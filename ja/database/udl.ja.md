{
  "date" : "2021-06-21",
  "keywords" :[ "UDL","拡張子","udl ファイル","udl ファイル形式","データベース ファイルの種類","データベース ファイル形式","udl ファイルとは" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"UDL ファイルの形式と,UDL ファイルを作成して開くことができる API について学びます。",
  "title" :"UDL - Microsoft ユニバーサル データ リンク ファイル",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## .UDL オプション番号
拡張子が .udl のファイルは、Microsoft Universal Data Link ファイルと呼ばれます。接続属性の指定; Windows アプリがデータベースとの接続を確立するために使用します。 UDL ファイルには、OLE DB データ ソースの接続文字列が含まれています。ユーザー名とパスワード、および重要な接続文字列のプロパティを使用します。接続文字列で手動でプロパティを直接指定することを避けるために、代わりに [データ リンク プロパティ] ダイアログ ボックスを使用して接続情報を .udl ファイルに保存することができます。

## UDL ファイル形式
基本的に、UDL (Universal Data Link) ファイルは、特定の属性またはプロパティを持つデータベース接続文字列で構成される単純なテキスト ファイルです。 UDL ファイルが作成されたら、SQL Server Management Studio を使用してテストし、接続を確認できます。

### 接続文字列のプロパティ
次のプロパティを UDL に設定して、適切な接続を確保できます。

- **サーバー名**: アクセスするデータベースがあるサーバーの場所。
- **認証オプション**
- **Windows 認証**: 現在ログインしているユーザーの Windows アカウント資格情報を使用した SQL Server への認証。
- **SQL Server 認証**: ログイン ID とパスワードを使用した認証。
- **Active Directory - 統合**: Azure Active Directory ID による統合認証。 SQL Server に対する Windows 認証にも使用できます。
- **Active Directory - パスワード**: Azure Active Directory ID によるユーザー ID とパスワード認証。
- **Active Directory - MFA をサポートするユニバーサル**: Azure Active Directory ID による対話型認証。
- **Active Directory - サービス プリンシパル**: Azure Active Directory サービス プリンシパルによる認証。
- **サーバー SPN**: 信頼された接続を使用する場合は、サーバーのサービス プリンシパル名 (SPN) を指定できます。
- **ユーザー名**: データ ソースへのサインイン時に認証に使用するユーザー ID を入力します。
- **パスワード**: データ ソースへのサインイン時に認証に使用するパスワードを入力します。
- **空白のパスワード**: オンにすると、指定したプロバイダーが接続文字列で空白のパスワードを使用できるようになります。
- **パスワードの保存を許可**: パスワードを接続文字列と共に保存できるようにします。
- **データに強力な暗号化を使用**: 接続を介して渡されるデータは暗号化されます。
- **Trust server certificate**: サーバーの証明書が検証されます。
- **データベース**: アクセスするデータベース名。
- **データベース ファイルをデータベース名として添付**: 添付可能なデータベースのプライマリ ファイルの名前を指定します。

## 参照 ##

* [Microsoft データ アクセス コンポーネント](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [ユニバーサル データ リンク (UDL) 構成](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

