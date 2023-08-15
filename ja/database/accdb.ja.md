{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDB ファイル形式と,ACCDB ファイルを作成して開くことができる API について学びます。",
  "title" :"ACCDB ファイル形式 - Microsoft Access 2007 データベース ファイル",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## .ACCDB ファイルとは?

拡張子が .accdb のファイルは、ユーザー データをテーブルに格納する Microsoft Access 2007 データベース ファイルです。収納にも対応
カスタム フォーム、SQL クエリ、およびその他のデータ。 Microsoft が XML ベースのファイル構造に移行した後、ACCDB ファイルは [MDB](/database/mdb/) ファイルに取って代わりました。 ACCDB ファイルは、古い互換性を持つ MDB に引き続き変換できます。ただし、ACCDB は現在広く使用されている Access データベース ファイル形式です。 Microsoft は、添付ファイルの保存、バイナリ データ、複数値フィールドのサポートなど、ACCDB 形式の追加機能もサポートしています。

## ACCDB ファイル形式

MDB と同様に、ACCDB ファイル形式で利用できる公開仕様はありません。 Microsoft は、Open Database Connectivity (ODBC) 標準および Visual Basic for Applications (VBA) を介したプログラムによるこれらのファイルへのアクセスをサポートしています。

### 洞察

単純な ACCDB ファイルの 16 進ダンプは、前身の MDB フォーマット ファミリの最新バージョンと構造が一般的に類似していることを示しています。どちらのファイル形式も、4096 バイトの固定ページ サイズを使用します。 ACCDB と MDB のもう 1 つの類似点は、ACCDB の文字列「Standard ACE DB」を含むマジック ナンバーの形式です。バージョンまたは互換性コードは、両方の形式で同じ場所にあります。 mdbtools | HACKINGファイルには、「オフセット0x14には、このデータベースのJetバージョンが含まれています」と記載されており、非公式のMDBガイドも同意しています。 [Microsoft Jet データベース エンジン](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) のウィキペディア エントリと組み合わせたこれらのソースの情報は、0x02 の値が ACE 12 (Access 2007) を示し、0x03 が ACE を示すことを示唆しています。 14 (アクセス 2010)。ただし、Access 2010 で作成された最小限のデータベースと、Access 2016 で作成された同様のデータベースでは、どちらもこの場所に 0x02 があります。 Access 2016 で作成された最小限のデータベースで、新しく導入された "大きな整数" データ型で列を定義すると、値が 0x05 になりました。 ACCDB ファイルでは、このインジケータは、ファイルの作成に使用された ACE エンジンのバージョンではなく、ファイルの互換性を反映しているように見えます。

## 参考文献

* [アクセス ファイル形式](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Access 2016 仕様](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet データベース エンジン](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [どの Access ファイル形式を使用すればよいですか?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
