{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG ファイル形式 - ESRI コード ページ ファイル",
  "description":"CPG ファイル形式と,CPG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## .CPGファイルとは?

CPG ファイルは、使用する文字セットを識別するためのコードページを指定するために使用される ESRI Shapefile に必要なオプション ファイルです。これらはプレーン テキスト ファイル形式で保存され、シェープファイルの作成に適用されたエンコーディングに関する情報が含まれています。 CPG ファイルが利用できない場合、シェープファイルはシステムのデフォルトのエンコーディングを使用します。 CPG ファイルが存在する場合、[SHP](/gis/shp/) ファイルと同じ接頭辞が必要です。たとえば、roads.shp、roads.cpg のようになります。

CPG ファイルは、ESRI ArcGIS Pro で開くことができます。

### CPG ファイル形式 - 詳細情報

ArcCatalog またはその他の ArcGIS アプリケーションでシェープファイルを表示すると、シェープファイルのみが表示されます。しかし実際には、シェープファイルはメインのシェープ ファイルと一緒に読み込まれる他の関連ファイルを使用します。メインの SHP ファイルと一緒に存在する場合、CPG ファイルもこれらの 1 つです。

## 参考文献

* [シェープファイルのファイル拡張子
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

