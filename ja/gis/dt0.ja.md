{
  "date" : "2022-12-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DT0 ファイル - DTED レベル 0 ファイル形式",
  "description":"DT0 ファイル形式と,DT0 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DT0",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-07"
}

## .DT0 オプション番号

DT0 ファイルは、地形標高データを調査するためのレベル 0 情報を含むデジタル地形標高データ (DTED) ファイルです。標高データは DT0 ファイルに均一に配置され、ESRI ArcGIS Pro、TatukGIS、Blue Marble Geographic Global Mapper、Pitney Bowes MapInfo などの一般的な GIS プログラムで読み取ることができます。 DT0 ファイルは主に科学および技術コミュニティによって使用され、地球規模の地形の勾配、標高、および表面の粗さを研究します。

DT0 ファイル形式は、[DT1](/ja/gis/dt1/) および [DT2](/ja/gis/dt2/) ファイル タイプに似ていますが、粒度が低くなります。

### DT0 ファイル形式

DT0 ファイルはバイナリ ファイルとしてディスクに保存されます。これらは、多くの GIS アプリケーションを使用して読み取ることができます。 DT0 ファイルは、1 つの大きなモザイクの作成に使用できるファイル ジオデータベース ラスター カタログにマージできます。

## ラスターを DTED ファイルに変換する方法は?

ラスターを DTED ファイルに変換できるツールは複数あります。 [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) は、Raster を DTED に変換できるツールの 1 つです。 .

## 参考文献

* [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
* [KML ファイル形式](/ja/gis/kml/)

