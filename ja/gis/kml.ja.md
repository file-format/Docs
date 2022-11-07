{
  "date" : "2019-10-11",
  "keywords" :[ "kml ファイル", "kml ファイルとは", "ファイル", "kml の例", "kml ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - キーホール マークアップ言語",
  "description":"KML ファイル形式と,KML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## KML ファイルとは

KML、Keyhole Markup Language) には、地理空間情報が XML 表記で含まれています。 KML として保存されたファイルは、サポートされている地理情報システム (GIS) アプリケーションで開くことができます。 KML ファイル形式が国際標準として採用された後、多くのアプリケーションが KML ファイル形式のサポートを開始しました。 KML は、要素と属性がネストされたタグベースの構造を使用します。すべてのタグは大文字と小文字が区別され、[KML](https://developers.google.com/kml/documentation/kmlreference) リファレンスに従ってこれらのタグの順序に従うことが重要です。

## 簡単な歴史 ##

KML は、もともと Keyhole Earth Viewer として知られていた Google Earth で使用するために開発されました。 KLM は、2008 年に Open Geospatial Consortium によって国際標準として採用されました。形式は Google Earth で使用するために開発されたため、KML ファイルを表示および編集する最初の形式であるという特徴があります。時間の経過とともに、さまざまな言語のいくつかの API を含む KML ファイル形式のサポートを提供するプロジェクトがますます増えています。

## KML ファイル形式の仕様 ##

KML リファレンスは、完全なファイル形式の仕様を参照するための完全なガイドです。標準の KML ファイルは次のもので構成されます。

*目印
* 目印の説明的な HTML
* グラウンドオーバーレイ
*パス
* ポリゴン

これらに加えて、KML ファイルの高度なバージョンには次のものがあります。

* ジオメトリのスタイル
* ハイライトされたアイコンのスタイル
*スクリーンオーバーレイ
* ネットワーク リンク

各 KML 要素には、ファイル内に存在する情報を地理的に特定する緯度経度情報があります。ただし、ヘディング、高度、傾きなどの追加のパラメータが存在する場合があります。

### 目印 ###

地球の表面上の位置を表すために使用され、<Point>エレメント。以下は、目印が KML ファイルでどのように表現されるかの例です。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### 目印の説明的な HTML ###

目印の表現をさらに強化する追加情報を目印に関連付けることができます。このような情報には、リンク、フォント サイズ、スタイル、および色が含まれます。さらに、目印の一部となるテキストの配置と表も含まれます。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### グラウンドオーバーレイ ###

これらは、地球の表面への画像の重ね合わせを表します。の<icon>要素には、オーバーレイ画像ファイルへのリンクが含まれています。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### パス ###

パスは<LineString>緯度と経度のペアのコレクションである要素。これらを使用して、さまざまな種類のパスを Google Earth で作成できます。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML ファイルでの空間参照 ##

Geo-Locations に関する Geospatial ファイルに含まれる情報は、空間参照情報がなければ異なる意味を持つ可能性があります。デフォルトでは、KML ファイルの空間参照は、1984 年の World Geodetic System、WGS84 によって定義されています。

## 参照 ##

* [KML リファレンス](https://developers.google.com/kml/documentation/kmlreference)
* [KML の Google デベロッパー チュートリアル](https://developers.google.com/kml/documentation/kml_tut)
* [KML ファイル形式](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

