{
  "date" : "2019-10-11",
  "keywords" :[ "gpx ファイル", "gpx ファイルとは", "ファイル", "gpx の例", "gpx ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange ファイル形式",
  "description":"GPX ファイル形式と,GPX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .GPX オプション番号

拡張子が GPX のファイルは、アプリケーションとインターネット上の Web サービスとの間で GPS データを交換するための GPS Exchange 形式を表します。これは軽量の XML ファイル形式で、GPS データ、つまり複数のプログラムによってインポートおよび赤化されるウェイポイント、ルート、トラックが含まれています。 GPX ファイル形式はオープンで、さまざまなアプリケーションや GPS デバイスでサポートされています。このようなファイルからの GPS データは、地理空間用のマッピング アプリケーションに表示するために読み込むことができます。

## GPX ファイル形式 ##

GPX ファイルは、緯度と経度の位置データ、標高値、およびその他の記述情報で構成されています。位置データは 10 進度で表され、標高はメートルで表されます。 GPX ファイルの時刻は、ISO 8601 形式を使用した協定世界時 (UTC) です。 GPX ファイルを使用する利点は次のとおりです。

* GPX を使用すると、Windows、MacOS、Linux、Palm、および PocketPC 用のプログラムのリストが増え続けているため、データを交換できます。
* GPX は、簡単な Web ページまたは変換プログラムを使用して、他のファイル形式に変換できます。
* GPX は XML 標準に基づいているため、使用する新しいプログラム (Microsoft Excel など) の多くは GPX ファイルを読み取ることができます。
* GPX を使用すると、Web 上の誰でも、お気に入りのプログラムですぐに動作する新機能を簡単に開発できます。

[GPX スキーマ](https://www.topografix.com/GPX/1/1/gpx.xsd) は、参照用に GPX ファイル形式の表現を示しています。

### 基本データ ###

以下は、GPS データを表す GPX ファイルの一部である重要なデータです。

* **ウェイポイント**: ウェイポイントはポイントの WGS84 (GPS) 座標であり、OGR タイプ wkbPoint のフィーチャのレイヤーを表します
* **ルート**: OGR タイプ wkbLineString のフィーチャのレイヤーを表します。これには、目的地につながるターンまたはステージ ポイントを示すウェイポイントであるトラック ポイントのリストが含まれます。
* **トラック**: トラックは、OGR タイプ wkbMultiLineString のフィーチャのレイヤーを表します。これは、パスを記述するポイントの順序付きリスト内のウェイポイントを含む少なくとも 1 つのセグメントで構成されます。これは、連続した GPS トラックを表すトラック ポイントのリストで構成されます。

### GPX サンプルファイル ###

次の GPX ファイルは、GPX ファイル内の GPS データの構成を示しており、GPX ファイルの内容についてよく理解できます。

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## 参照 ##

* [GPX ファイル形式](https://www.topografix.com/gpx.asp)
* [GPX - ウィキペディアによる](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

