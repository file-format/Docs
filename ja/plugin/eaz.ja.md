{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ ファイル - EAZ ファイルとは何ですか?またその開き方は?",
  "description":"EAZ ファイル形式と、EAZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-jaz"
}
},
  "lastmod" : "2023-12-23"
}

## .EAZ ファイルとは何ですか?

EAZ ファイルは、マップ探索、視覚化、共有のために ESRI によって開発された無料のアプリケーションである ArcGIS Explorer で利用されるアドイン ファイルです。これには、[XML file](/web/xml/)、コンパイルされたコード、アドインに必要なサポート ファイルを含む圧縮ファイル アーカイブが含まれています。これらのファイルは、新しいボタン、ドッキング可能なウィンドウ、その他の拡張機能を組み込むことでソフトウェアの基本機能を拡張するために使用されます。

## EAZ ファイル形式 - 詳細情報

EAZ ファイルは、ArcGIS Explorer 内でカスタム機能を作成するために設計された開発キットである ArcGIS Explorer SDK を利用して作成されます。これらのファイルは、[ZIP](/compression/zip/) 圧縮を利用してコンテンツを効率的にパッケージ化します。アーカイブの中核となる **Addins.xml** ファイルはルート ディレクトリにあり、EAZ ファイルに埋め込まれたさまざまなカスタマイズの概要と詳細を説明する重要なコンポーネントとして機能します。

Addins.xml ファイルは基本的にロードマップとして機能し、EAZ ファイルによって ArcGIS Explorer に導入される特定の機能強化、変更、拡張機能についての洞察を提供します。この包括的な構造を通じて、開発者は新しい機能、ボタン、ドッキング可能なウィンドウをカプセル化してシームレスに統合し、ArcGIS Explorer アプリケーションの全体的な機能とユーザー エクスペリエンスを向上させることができます。

## 参考文献

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
