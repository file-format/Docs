{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"3DM ファイル形式と,3DM ファイルを開いて作成できる API について学びます。",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## 3DM ファイルとは?

拡張子が .3dm のファイルは、3D グラフィック ソフトウェアで使用されるオープン ソースのファイル形式です。これには、サーフェス、ポイント、曲線情報などの依存要素とともに 3D モデルが含まれています。 3DM ファイル形式は、[openNURBS](https://github.com/mcneel/opennurbs) イニシアチブによって、アプリケーション間で 3D ジオメトリを正確に転送するために開発されました。 3DM ファイルは、Rhinoceros、SAP VEViewer、Moment of Inspiration、Right Hemisphere Deep View などのアプリケーションで開いて変換できます。

## 3DM ファイル形式

オープンソースのツールキットである [openNURBS](https://github.com/mcneel/opennurbs) には、3DM ファイル形式の仕様、ドキュメント、C++ ソース コード ライブラリ、およびファイル形式を読み書きするための .NET 2.0 アセンブリが含まれています。

### 3DM サンプル ファイル

いくつかのサンプル 3DM ファイルは、openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) セクションからダウンロードできます。これらは、openNURBS ツールキットを使用してロードおよび表示できます。

## 3DM ファイルを読み書きするには?

[openNURBS](https://github.com/mcneel/opennurbs) ライブラリを使用すると、Rhino を必要とせずに、誰でも 3DM ファイル形式を読み書きできます。 openNURBS ファイル形式を使用して 3D モデルを読み書きするライブラリの C++ ソース コードを提供します。このツールキットには、NURBS 評価ツール、基本的なジオメトリおよび 3D ビュー操作ツールも含まれており、いくつかのサンプル プログラムのソース コードも含まれています。 [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) サポート フォーラムは、3DM コミュニティが直面している問題を共有し、解決策を得るための豊富なコンテンツとディスカッションの場です。

## 参照 ##

* [サイ](https://www.rhino3d.com/download/openNURBS)
* [サイ - ウィキペディア](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [GitHub の openNURBS](https://github.com/mcneel/opennurbs)

