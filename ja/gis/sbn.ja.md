{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - ESRI 空間インデックス バイナリ ファイル",
  "description":"SBN ファイル形式と,SBN ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## .SBN ファイルとは何ですか?

拡張子が .sbn のファイルは、ESRI ArcGIS [.shp](/gis/shp/) ファイルに関連付けられている空間インデックス ファイルです。データに対してインデックスが実行されたときに、空間クエリを最適化するために使用されます。 .sbn と共に使用される他のファイル タイプは .sbx ファイルです。 SBN ファイルと SBX ファイルを組み合わせてシェイプ インデックスを構成し、空間クエリを高速化します。 SBN ファイルはオプションであり、[ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview) で開くことができます。

## SBN ファイル形式 - 詳細情報

SBN ファイルはバイナリ ファイルとしてディスクに保存され、内部ファイル形式の詳細は利用できません。これらには、空間クエリ用の SHP ファイルのバイナリ表現が格納されます。 SBX インデックス ファイルは、シェープファイルの空間クエリを高速化するために SBN ファイルと共に使用されます。

## 参考文献

* [ESRI ShapeFile 技術説明](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

