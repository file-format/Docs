{
  "date" : "2019-10-11",
  "keywords" :[ "qlr ファイル", "qlr ファイル形式", "qlr ファイルとは", "ファイル", "qlr の例", "qlr ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS レイヤー定義ファイル",
  "description":"QLR ファイル形式と,QLR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## .QLR ファイルとは何ですか?

.qlr を含むファイルは、レイヤー データ ソースへのポインターを含むレイヤー定義ファイルです。これは、レイヤーの [QGIS](https://www.qgis.org/en/site/) スタイル情報に追加されます。関連するすべてのスタイルへの参照を持つこのファイルは、スタイル情報を取得するために使用されるデータの単一ソースとして使用されます。 QLR ファイルを使用すると、データ ソースへの情報をこの 1 つのファイルに入れることができ、他のアプリケーションがこのファイルを読み取ってスタイリング情報を読み込むことができます。 QLR ファイルは、Notepad++ などの任意のテキスト エディターで開くことができます。

## QLR ファイル形式

[QGS](/gis/qgs/) に似た QLR は、レイヤー データ ソースへのポインターを XML タグの形式で含む XML ファイルです。これは、ArcGIS .lyr ファイルに似ています。 QML ファイルの最上位のタグは、下の画像に示すとおりです。

{{< figure src="../qlr.png" title="" >}}

## 参考文献

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

