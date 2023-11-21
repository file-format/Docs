{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD ファイル - ASP.NET Web ハンドラー ファイル形式",
  "description" :"AXD ファイルとは何か,および AXD ファイルを作成して開くことができる API について説明します。",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## .AXD ファイルとは何ですか?

AXD ファイルは、ASP.NET で埋め込みリソース要求を処理および取得するために使用される Web 設定ファイルです。これは、画像、JavaScript ([.JS](/ja/web/js/)) ファイル、[.CSS](/ja/web/css/) ファイルなどの埋め込みリソースを取得するための命令で構成されます。 AXD ファイルは、クライアント側のページにリソースを挿入するために使用されます。これにより、クライアント ページが標準的な方法でサーバー上のこれらのリソースにアクセスできるようになります。

## AXD ファイル形式

AXD ファイルは、サーバー側にバイナリ ファイルとして保存されます。これは、Web サーバーへの特定の要求に対する応答を生成するコンポーネントである ASP.NET の Web ハンドラー ファイルを指します。 AXD ファイルは、クライアント側のページ要求に基づいて応答を生成する前に、カスタム処理を実行します。これらは通常、**WebResource.axd** ファイルとして保存されます。

### WebResource.axd ファイルとは何ですか?

ほとんどの ASP.NET プロジェクトは、AXD ファイルを WebResource.axd ファイルとして保存し、クライアント側のページがアセンブリに埋め込まれているリソースをダウンロードできるようにします。 WebResources.axd ハンドラーがキャッシュされていないため、アプリケーションをデバッグ モードで実行すると、パフォーマンスが低下する可能性があります。

## 参考文献

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

