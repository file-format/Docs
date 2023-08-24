{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DISCOファイル - DISCOディスカバリードキュメントファイル形式",
  "description":"DISCO ファイルとは何か,および DISCO ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## .DISCO ファイルとは何ですか?

DISCO ファイルは、Web サービスの公開と検出に使用される Microsoft Discovery ファイル形式です。これは XML ファイル形式で保存され、Web Services Discovery ツールが、利用可能な [XML](/web/xml/) サービスを説明するための 1 つ以上の関連ドキュメントを検索または検出できるようにします。 DISCO ファイルには、検出ドキュメント、[XSD](/programming/xsd/) スキーマ、サービスの説明などの情報が保存されます。 XML Web サービスは、この情報を使用して、特定の URL で利用可能な XML Web サービスにアクセスします。

## DISCO ファイル形式 - 詳細情報

DISCO ファイルは XML ファイル形式で保存されます。 Microsoft Studio などの Microsoft ASP.NET 開発ソフトウェアにバンドルされている Microsoft Discovery Tool (DISCO.exe) は、DISCO ファイルを使用して、特定の URL の DiscoveryDocument にリストされている XML Web サービスに関する詳細を検出します。 Microsoft は、.NET フレームワークでの検出ファイルの読み取りをサポートしています。

## 参考文献

* [ディスコ](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web サービスの発見](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# DiscoveryClient クラスの例](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

