{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO ファイル - DISCO ダイナミック ディスカバリ ドキュメント ファイル形式",
  "description":"VDISCO ファイルとは何ですか?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## VDISCO ファイルとは何ですか?

VDISCO ファイルは、Microsoft Visual Studio の Web サービスで使用される検出ファイルです。 URL、名前空間、メソッドなど、利用可能な Web サービスに関する情報を提供します。 VDISCO ファイルは [DISCO](/ja/web/disco/) ファイル形式に似ていますが、実行時に生成されます。これは Web サービス アプリケーションに保存され、プロジェクト内の Web サービスを動的に検出して使用するために Visual Studio によって使用されます。 VDISCO ファイルは、実際の Web サービス コードを含む [.asmx](/ja/web/asmx/) ファイルと組み合わせて使用されます。

VDISCO ファイルは、Microsoft Notepad、Github Atom、Apple TextEdit などのテキスト エディタで開くことができます。 Microsoft Visual Studio 2012 以降で開いて作業することもできます。

## VDISCO ファイル形式

VDISCO ファイルは、データの作成と公開のための汎用形式である [XML](/ja/web/xml/) ファイル形式で保存およびホストされます。これには、標準 XML タグ内のサービス URL、名前空間、およびメソッドが含まれており、各タグにはその情報のそれぞれの値が含まれています。

## 参考文献

* [ディスコ](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web サービス ディスカバリー](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [DiscoveryClient クラスの C# 例](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

