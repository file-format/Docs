{
"日付": "2023-09-27",
  "keywords": [
"cfg",
"cfg ファイル",
"cfg Celestia 設定ファイル",
"cfg ファイルとは何ですか",
"cfg ファイルを開く方法",
"ファイル",
"cfg ファイル拡張子",
"拡大"
],
  "author": {
"display_name": "シェキール・ファイズ"
},
"ドラフト": "偽",
"toc": true,
"title": "CFG ファイル形式 - Celestia 設定ファイル",
  "description":"CFG Celestia 構成ファイル形式と,CFG ファイルを作成して開くことができる API について学びます。",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent":"settings"
}
},
"lastmod": "2023-09-27"
}

## .CFG オプション番号は何ですか?

Celestia 設定ファイルは、3D 宇宙シミュレーション プログラム Celestia で使用されるプレーン テキスト ファイルです。これらのファイルは、Celestia の動作、表示される天体、プログラムの表示方法をカスタマイズするために不可欠です。ただし、不適切な変更を行うと Celestia の読み込みプロセスが中断され、正常に実行できなくなる可能性があるため、これらのファイルの編集には細心の注意が必要です。

## セレスティア

Celestia は、ユーザーが非常に現実的かつインタラクティブな方法で宇宙を探索および視覚化できる、無料のオープンソース 3D 天文学シミュレーション ソフトウェアです。 Chris Laurel によって開発され、2000 年代初頭に初めてリリースされました。 Celestia は、Windows、macOS、および Linux オペレーティング システムで利用できます。

Celestia の主な機能と側面は次のとおりです。

- **リアルな 3D ビジュアライゼーション:** Celestia は、太陽系、星、銀河、その他の天体を詳細かつ正確に表現します。高品質の 3D モデルとテクスチャを使用して、視覚的に没入型のエクスペリエンスを作成します。

- **広範な天体データベース:** このソフトウェアには、星、惑星、月、小惑星、彗星、宇宙船などの既知の天体の膨大なデータベースが組み込まれています。ユーザーはこれらのオブジェクトを簡単に見つけて探索できます。

- **科学的精度:** Celestia は視覚化ツールですが、利用可能な科学データに基づいて、天体や現象をできるだけ正確に表現することを目的としています。

## Celestia で使用されるファイル形式

Celestia は、3D 天文シミュレーションのさまざまな側面にさまざまなファイル形式を利用しています。 Celestia で採用されている主なファイル形式の一部を次に示します。

1. **設定ファイル (.cel)**
- *説明*: ユーザーが Celestia の動作、外観、コンテンツをカスタマイズできるプレーン テキスト ファイル。
- *目的*: 設定のカスタマイズ、場所の定義、天体の指定。

2. **3D モデルとメッシュ**
- *形式*: [.3ds](/ja/3d/3ds/)、[.obj](/ja/3d/obj/)、[.dae](/ja/3d/dae/)、.ac
- *説明*: 天体や宇宙船のレンダリングに使用される 3D モデル ファイル形式をサポートしました。
- *目的*: Celestia 内で 3D オブジェクトを表示します。

3. **テクスチャ ファイル**
- *形式*: [.jpg](/ja/image/jpeg/)、[.png](/ja/image/png/)、[.dds](/ja/image/dds/)
- *説明*: これらのファイルは、天体の表面テクスチャを提供します。
- *目的*: テクスチャを 3D モデルにマッピングして、リアルな外観を実現します。

4. **スターカタログとデータファイル**
- *形式*: カスタム形式、[.csv](/ja/spreadsheet/csv/)、[.tsv](/ja/spreadsheet/tsv/)
- *説明*: 星やその他の天体を表すために使用されるデータ ファイルで、正確なシミュレーションを保証します。
- *目的*: 天体の正確な表現。

5. **テクスチャ キューブ マップ**
- *説明*: キューブ マップは、銀河などの遠方の天体の外観をシミュレートするために使用されます。
- *目的*: 遠くのオブジェクトをリアルなテクスチャでレンダリングします。

6. **スクリプト ファイル**
- *説明*: これらのファイルには、Celestia のスクリプト言語で書かれたカスタム スクリプトが含まれています。
- *目的*: ユーザーが Celestia のユニバース内で動的なイベントやアニメーションを作成できるようにします。

## Celestia 設定ファイル

Celestia 設定ファイルでできることの基本的な概要は次のとおりです。

1. **位置の設定**: 緯度、経度、高度のパラメーターを使用して、地球上の位置を指定できます。これにより、Celestia はあなたの位置からの夜空を正確に表示できるようになります。

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **表示オプションのカスタマイズ:** 視野、時間設定、レンダリング設定などのさまざまな表示オプションを調整できます。

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **天体の読み込み:** 星、惑星、小惑星、宇宙船などの天体をシミュレーションに追加できます。各オブジェクトは、そのプロパティとともに構成ファイルで定義されます。

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **宇宙船の定義:** 独自の架空の宇宙船を作成したり、位置、方向、3D モデルなどのパラメータを指定して実際の宇宙船を使用したりできます。

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **スクリプトの作成:** Celestia のカスタム スクリプト言語でスクリプトを作成し、動的なイベントやアニメーションを作成できます。

## CFGファイルを開くにはどうすればよいですか?

CFG ファイルを開いたり参照したりするプログラム

- Celestia (無料) (Windows、Mac、Linux)

## その他の CFG ファイル

**.cfg** ファイル拡張子を使用する他のファイル タイプは次のとおりです。

**設定**
- [CFG - Celestia 設定ファイル](/ja/settings/cfg-celestia/)
- [CFG - Citrix サーバー接続ファイル](/ja/settings/cfg-citrix/)
- [CFG - MAME設定ファイル](/ja/settings/cfg-mame/)
- [CFG - LightWave設定ファイル](/ja/settings/cfg-lightwave/)

**ゲーム**
- [CFG - Wesnoth マークアップ言語ファイル](/ja/game/cfg-wesnoth/)
- [CFG - MUGEN設定ファイル](/ja/game/cfg-mugen/)
- [CFG - ソースエンジン設定ファイル](/ja/game/cfg-sourceengine/)

**システムとその他**
- [CFG - CFGファイル](/ja/system/cfg/)
- [CFG - Cal3D モデル設定ファイル](/ja/misc/cfg-cal3d/)

## 参考文献
* [セレスティア](https://en.wikipedia.org/wiki/Celestia)

