{
  "date" : "2019-10-11",
  "keywords" :[ "qml ファイル", "qml ファイル形式", "qml ファイルとは", "ファイル", "qml の例", "qml ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - QGIS スタイル ファイル形式",
  "description":"QML ファイル形式と,QML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## .QML ファイルとは?

拡張子が .qml のファイルは、QGIS レイヤーのレイヤー スタイル情報を格納する XML ファイルです。 QGIS は、レイヤーの形式でデータを整理する機能を備えた地理空間データを表示するために使用される、オープンソースのクロスプラットフォーム GIS アプリケーションです。 QML ファイルには、シンボル定義、サイズと回転、ラベリング、不透明度、ブレンド モードなどを含むフィーチャ ジオメトリをレンダリングするために QGIS によって使用される情報が含まれています。 QLR ファイルとは異なり、QML ファイルにはすべてのスタイル情報が含まれています。 QML ファイルは、Notepad++ などの任意のテキスト エディターで開くことができます。

## QML ファイル形式

[QGS](/gis/qgs/) および [QLR](/gis/qlr/) と同様に、QLR はレイヤーのスタイル情報を含む XML ファイルです。

下の図は、QML ファイルのトップ レベルのタグを示しています (renderer_v2 とそのシンボル タグのみが展開されています)。

{{< figure src="../qml.png" title="" >}}

## 参考文献

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

