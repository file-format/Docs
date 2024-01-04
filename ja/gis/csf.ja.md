{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSF ファイル - GeoMedia 座標系ファイル形式",
  "description":"CSF ファイル形式と,CSF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## .CSF ファイルとは何ですか?

CSF ファイルは、GIS ファイルの座標系に関する情報が含まれる座標系ファイルです。これは、特定の座標系のパラメーターを定義するために Intergraph の GeoMedia ソフトウェアによって使用されます。これらには、データム、投影法、測定単位などの情報パラメーターが含まれます。この情報は、座標系が設定されていない出力データのマップを作成するために使用されます。この情報は、地理データを正しい座標系で正しく表示および操作するために GeoMedia によって使用されます。

## CSF ファイル形式

CSF ファイルは、地理座標系の詳細を含むテキスト ファイルとして保存されます。 GeoMedia を使用すると、座標系が定義されていない入力データから地理情報ファイルをインポートできます。 GIS システムは、投影法と座標系を使用して、正確な値を含むマップ ファイルを表示します。 CSF ファイルは出力ファイルと同じ場所に作成されます。

## 参考文献

* [シェープファイル データを GeoMedia に正しく表示または提供するにはどうすればよいですか?](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)

