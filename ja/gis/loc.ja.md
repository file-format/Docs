{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "file", "extension", "file format", "GPS Location", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS ロケーション ファイル形式",
  "description":"LOC ファイルのフォーマットと,LOC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## .LOC オプション番号

拡張子が .loc のファイルは、ウェイポイントとして地理空間的な場所を含む GPS ロケーション ファイルです。ウェイポイントは、地理情報システム (GIS) アプリケーションで使用される場所を参照する緯度と経度の値のペアです。 DeLorme Topo などの GPS マッピング プログラムは、LOC ファイルを使用して、これらの LOC ファイルに含まれる情報を読み取り、エンド ユーザーが選択可能なレイヤーとして表示します。さらに、これらはアプリケーション間で GPS データを交換するために使用されます。 LOC ファイルは、[TopoGrafix EasyGPS](https://www.easygps.com/) などのアプリケーションを使用して開くことができます。このアプリケーションは、そのようなファイルの内容を、それぞれのジオロケーションでマップ上にプロットされたレイヤーやデータとして表示します。

## LOC ファイル形式 - 詳細情報

LOC ファイルは [GPX](/gis/gpx/) ファイルと似ていますが、異なる形式で保存されます。これらは [XML](/web/xml/) ファイルとして保存され、ウェイポイントのコンテンツと関連情報が構造化タグに含まれています。 XML は異なるアプリケーション間でデータを交換するための一般化された言語であるため、他のアプリケーションとの LOC データの交換が容易になります。

## LOC ファイル形式 - 例

以下は、LOC ファイルからの 1 つのウェイポイントのヘッダーとテキストです。ご覧のとおり、ヘッダー情報にはデータの場所のソースが含まれています。ウェイポイントには、「ID」などの情報と、ウェイポイントに関連付けられた関連コンテンツ データが含まれています。最後に、ウェイポイントは、緯度と経度の値と、この特定のウェイポイントに関連付けられたテキストのコレクションです。

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## 参考文献

* [TopGraphic EasyGPS](https://www.easygps.com/)

