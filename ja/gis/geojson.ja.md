{
  "date" : "2019-10-11",
  "keywords" :[ "geojson ファイル","geojson ファイルとは","ファイル","geojson の例","geojson ファイルの拡張子","拡張子","形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - JSON ベースの地理ファイル形式",
  "description":"GeoJSON ファイル形式と,GeoJSON ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## GeoJSON ファイルとは?

GeoJSON は、地理的特徴を非空間属性で表すように設計された JSON ベースの形式です。この形式は、さまざまな JSON (JavaScript Object Notation) オブジェクトとそれらの結合方法を定義します。 JSON 形式は、地理的特徴、その空間範囲、およびプロパティに関する集合情報を表します。このファイルのオブジェクトは、ジオメトリ (ポイント、ラインストリング、ポリゴン)、フィーチャ、またはフィーチャのコレクションを示す場合があります。フィーチャは、住所と場所をポイントの通りとして、幹線道路と国境をライン ストリングとして、国、州、および地域をポリゴンとして反映します。 GeoJSON を使用すると、さまざまなモバイル ルーティングおよびナビゲーション アプリケーションがサービスの範囲を示すことができます。 GeoJSON の拡張機能は、サイズが小さく、地理空間トポロジをエンコードする TopoJSON です。

## 簡単な歴史 ##

Internet Engineering Task Force (IETF) は、フォーマットの作成者と協力して、[GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) を形成し、2015 年 4 月に GeoJSON をリリースしました。 GeoJSON 仕様、[RFC 7946](https://tools.ietf.org/html/rfc7946)、2016 年 8 月に公開された GeoJSON 形式の新しい標準仕様。

## GeoJSON ファイル形式 ##

### 座標 ###

座標は、地理データの基本要素です。これは、単一の数値 (10 進数形式) を表す単一の次元 (経度、緯度) であり、標高の座標も記録する場合があります。時間も次元ですが、その複雑さが座標として記録することを困難にしています。両方の JSON GeoJSON の座標は、数値のようにフォーマットされます。

＃＃＃ 位置 ＃＃＃

[位置](http://geojson.org/geojson-spec.html#positions)を表す座標の順序付き配列。これは、地球上の点を示すことができる最小単位です。

`[経度、緯度、標高]`

現在の仕様がリリースされる前は、GeoJSON は位置ごとに 3 つの座標を記録できましたが、新しい仕様では許可されていません。

### ジオメトリ ###

ジオメトリは、タイプと座標のコレクションで構成される GeoJSON の単純な形状 (ポイント、カーブ、およびサーフェス) です。ポイントは、単一の位置を表す最も単純なジオメトリです

`{ "タイプ": "ポイント", "座標": [0, 0] }`

### ラインストリング ###

線を表すために、少なくとも 2 つの接続された場所が使用されます。

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

ポイント ストリングとライン ストリングは、ジオメトリの 2 つの最も単純なカテゴリです。どちらのタイプのジオメトリも、多くの幾何学的ルールを気にしません。点は任意の場所に表すことができ、点が自己交差している場合でも、線は複数の点を持つことができます。

### ポリゴン ###

GeoJSON ジオメトリは、Polygon ではかなり複雑に見えます。ポリゴンには内側と外側の領域があり、その内側に穴を持つことができます。

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

LineString と比較して、ポリゴンでは、座標のリストがもう 1 レベルネストされており、ドーナツのようなカットアウトを持つことができます。

### 座標レベル ###

GeoJSON 形式の座標プロパティには、4 つのレベルの深さがあります。

＃＃＃ 特徴 ＃＃＃

ジオメトリは GeoJSON の中心部分であるため、現実世界のデータは、ID と属性を持つこれらの単純な形状以上のものです。フィーチャは、ジオメトリとそのプロパティを記録します。

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
}、
  "properties": {
    "name": "fortune island"
  }
}

```

機能プロパティは、[JSON](http://json.org/) オブジェクトのタイプであり、単一深度のキー値マッピングが含まれます。

### 機能コレクション ###

GeoJSON ファイルのトップ レベルで、FeatureCollection は次のような最も一般的なものです。

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    }、
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

GeoDjango、OpenLayers、Geoforge ソフトウェアなど、多くのマッピングおよび GIS ソフトウェア パッケージが GeoJSON をサポートしています。 PostGIS や Mapnik とも互換性があります。 Google、yahoo、および Bing マップの API サービスも GeoJSON をサポートしています。

## 参照 ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - ウィキペディアによる](https://en.wikipedia.org/wiki/GeoJSON)

