
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML ファイル - Microsoft アシスタンス マークアップ言語ファイル",
  "description":"AML ファイルとは何か,および AML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft アシスタンス マークアップ言語ファイル

## .AML ファイルとは?

AML (Assistance Markup Language) ファイルは、Microsoft Assistance Markup Language (MAML) で生成された XML ファイルです。これは、Microsoft Windows OS のオンライン ヘルプを提供するために Microsoft によって開発されました。これ以前は、Windows ヘルプはコンパイルされた HTML [CHM](/web/chm/) ファイル形式で利用できました。 AML ファイルは、アプリケーションがソース コードとサポート ヘルプ ページを作成できる構造化ドキュメントを提供します。これにより、ドキュメントとその構成要素をコンテキストによって定義できます。 AML ヘルプ ファイルはオンラインで公開されており、オンラインで入手可能なパッケージ更新から更新されるように構成できます。

## MAML ファイル構造

MAML を使用して生成された AML ファイルは [XML](/web/xml/) ファイルとして保存され、幅広いアクティブな概念を表現するために使用できます。また、ガイド付きヘルプ (アクティブ コンテンツ ウィザード) を提供することもできます。このヘルプ ファイルは、段階的なウィザードを使用してユーザー向けにインタラクティブになります。

MAML を使用して生成された AML ファイルは、次のようなセグメントに分割できるオーサリング構造に従います。

*概念的
* よくある質問
*用語集
* 手順
* 参照
* 再利用可能なコンテンツ
* 仕事
* トラブルシューティング、および
* チュートリアル

## MAML ファイルの作成方法

MAML ファイルは、次のいずれかの方法で作成できます。

* Sandcastle の使用 - 一連のスキーマとプログラム実行可能ファイルを利用して、ヘルプ ファイルを生成します。ただし、このツールは廃止されました。
* DocProject の使用 - ヘルプ コンテンツを生成するために Microsoft Visual Studio 内から実行できる Microsoft Visual Studio プラグイン。

MAML ファイルは、.XSL スキーマとプログラム実行可能ファイルのスイートである Sandcastle を使用して作成できます。また、Microsoft Visual Studio ヘルプ オーサリング ツール アドインである DocProject を使用して作成することもできます。

## 参考文献

* [PlatyPS を使用して XML ベースのヘルプを作成する](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [マイクロソフト支援マークアップ言語](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc マクロ言語ファイル

## ARC マクロ AML ファイルとは?

AML (ARC マクロ言語) ファイルは、ArcInfo Workstation GIS アプリケーションで生成されるスクリプト ファイルです。これは、ArcInfo で GIS アプリケーションを作成するための独自の高レベル アルゴリズム言語である ARC マクロ言語で記述されています。 AML は 1986 年に ESRI によって設計され、コマンド ライン ARCINFO GIS システムからアプリケーションを作成する目的で使用されました。スクリプト ファイルである AML ファイルには、ユーザー インターフェイス コンポーネントの作成やマップ データの操作など、さまざまなタスクを実行するためのスクリプト コマンドを含めることができます。

## AML ファイル形式 - 詳細情報

スクリプト ファイルである AML は、情報をプレーン テキスト ファイルとしてディスクに保存します。これは、PRIMOS オペレーティング システムの CPL シェル言語に基づく AML 構文に従います。 AML 言語は、ArcGIS スイートの一部であり、ArcObjects を使用して VBA または Python を介したプログラミング サポートを提供する ESRI のジオプロセシング フレームワークに置き換えられました。

## 参考文献

* [ARC マクロ言語](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [スクリプト ツールでの AML の使用](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

