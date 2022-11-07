{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx ファイル", "asmx ファイル形式", "asmx ファイルの種類", "ファイル", "種類", "asmx ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web サービス ファイル",
  "description" :"ASMX ファイルとは何か,および ASMX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASMX オプション番号

拡張子が .asmx のファイルは、Simple Object Access Protocol (SOAP) を使用してインターネット経由で 2 つのオブジェクト間の通信を提供する ASP.NET Web サービス ファイルです。これは、Windows ベースの Web サーバーにサービスとして展開され、着信要求を処理して応答を返します。 ASP.NET Web ページを視覚的に表示するためのコードを含む [ASPX](/web/aspx/) ファイルとは異なり、ASMX ファイルはサーバーでバックグラウンドで実行され、データベースへの接続、データの取得、データの取得などのさまざまなタスクを実行します。リクエストが行われた形式。これらは、特に XML Web サービスに使用されます。

## ASMX ファイル形式

ASMX ファイルはプレーン テキスト形式であり、Microsoft Visual Studio やテキスト エディターなどのアプリケーションで開いたり編集したりできます。これは Microsoft 独自のファイル形式であり、Web サービスを作成するための明確に定義された構文を備えています。 SOAP XML 形式の ASMX ファイルによる応答には、次の要素があります。

* `Envelop` - XML ドキュメントを SOAP メッセージとして識別するルート要素。
* `Header` - 認証データなどのアプリケーション固有の情報を含むオプションの要素。 Header 要素が存在する場合、それは Envelope 要素の最初の子要素である必要があります。
* `Body` - 受信者向けの SOAP メッセージが含まれます。
* `Fault` - エラー メッセージを示すために使用されるオプションの要素。 Fault 要素が存在する場合、それは Body 要素の子要素である必要があります。

ASMX ファイルは、[C#](/programming/cs/)、[Visual Basic](/programming/vb/)、または JScript などの .NET 言語で記述できます。

## ASMX は ASPX や ASCX とどう違うのですか?

ASMX ファイルは、ASPX および ASCX ファイルとは異なります。

* ASPX、Active Server Pages、ファイルは、Web サーバー上で動作する Microsoft ASP.NET フレームワークを使用して生成されるプログラミング ファイルです。これらは、ユーザーがそのようなページへのアクセスを要求すると、クライアントの Web ブラウザーでレンダリングされます。
* ASCX (Active Server User Control) は、ASP.NET Web ページまたは Web サイト全体で再利用可能なコントロールを定義するために使用されるユーザー コントロールを定義します。

## 参考文献

* [ASMX サービスの利用](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX ユーザー コントロール](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

