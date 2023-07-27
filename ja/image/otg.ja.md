{
  "date" : "2020-01-10",
  "keywords" :[ "otg ファイル", "otg ファイル形式", "otg ファイルとは", "ファイル", "otg の例", "otg ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument 図面テンプレート ファイル形式",
  "description":"OTG ファイル形式と,OTG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## .OTG オプション番号

OTG ファイルは、OASIS Office Applications [1.0 仕様](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf) に準拠した OpenDocument 標準を使用して作成された図面テンプレートです。 。これは、ファイルのコンテンツをさらに強化するために使用できる、ベクター イメージの描画要素の既定の編成を表します。 OTF ファイルは、ドキュメントの内容を表す XML 形式に基づく他の OpenDocument 形式ベースのファイルと同様です。 OTF ファイルは、任意のテキストまたは標準の XML エディターで開いて表示できます。

## OTG ファイル形式の仕様 ##

OTG ファイル形式は、十分に確立されたスキーマを持つ OpenDocument XML 形式に基づいています。 OpenDocument 形式の各コンポーネントの構造は、関連付けられた属性を持つ要素によって表され、テキスト ドキュメント、スプレッドシート、図面ファイルなどのすべてのドキュメント タイプに共通です。図面テンプレートである OTG は、以下を含むグラフィック コンテンツ仕様を広範に利用します。

* グラフィカル アプリケーション向けの強化されたページ機能
* 図形の描画
* フレーム
* 3D シェイプ
* カスタム形状
* プレゼンテーション形状
* プレゼンテーション アニメーション
* SMIL プレゼンテーション アニメーション
* プレゼンテーションイベント
* 現在のテキスト フィールド
※発表資料の内容

### グラフィカル アプリケーション向けの強化されたページ機能 ###
#### 配布資料マスター ####

配布資料マスター要素は、そのようなページの印刷をサポートするアプリケーション用の配布資料ページを自動的に生成するためのテンプレートです。
` に関連付けることができる属性<style:handout-master>`要素は次のとおりです。

|レイアウト|属性|説明
---|---|---|
|Presentation Page Layout|presentation:presentation-page-layout-name|`へのリンク<style:presentation-page-layout>` 属性
|ページ レイアウト|`style:ページ レイアウト名` |配布資料マスター ページのサイズ、境界線、および向きを含むページ レイアウトを指定します。
|ページ スタイル|`draw:style-name`|図面ページ スタイルを割り当てることにより、配布資料マスターページに追加の書式設定属性を割り当てます。|
|ヘッダー宣言| `presentation:use-header-name`|配布資料マスター ページに表示されるすべてのヘッダー フィールドに使用されるヘッダー フィールド宣言の名前を指定します。
|フッター宣言| presentation:use-footer-name|配布資料マスター ページに表示されるすべてのフッター フィールドに使用されるフッター フィールド宣言の名前を指定します。
|日時宣言|use-date-time-name|配布資料マスター ページに表示されるすべての日時フィールドに使用される日時フィールド宣言の名前を指定します。

### 図形の描画 ###
OpenDocument 形式は、あらゆる種類のドキュメントで使用できるいくつかの描画図形をサポートしています。

|形状|関連する属性|要素
---|---|---|
長方形 - `<draw:rect> `|位置、サイズ、スタイル、レイヤー、Z インデックス、ID、キャプション ID、テキスト アンカー、テーブルの背景、描画終了位置、角丸|タイトル、詳細な説明、イベント リスナー、接着点、テキスト
行 `<draw:line> `|スタイル、レイヤー、Z インデックス、ID、キャプション ID と変換、テキスト アンカー、テーブルの背景、描画終了位置、開始点、終了点|タイトル、詳細な説明、イベント リスナー、接着点、テキスト
ポリライン `<draw:polyline> | `|位置、サイズ、ビュー ボックス、スタイル、レイヤー、Z インデックス、ID、キャプション ID と変換、テキスト アンカー、テーブルの背景、描画終了位置、ポイント|タイトル、詳細な説明、イベント リスナー、グルー ポイント、テキスト
ポリゴン `<draw:polygon> `|位置、サイズ、ビュー ボックス、スタイル、レイヤー、Z インデックス、ID、キャプション ID と変換、テキスト アンカー、テーブルの背景、描画終了位置、ポイント|タイトル、詳細な説明、イベント リスナー、接着点、テキスト
|正多角形 `<draw:regular-polygon> `|位置、サイズ、スタイル、レイヤー、Z インデックス、ID、キャプション ID と変換、テキスト アンカー、テーブルの背景、描画終了位置、凹面、コーナー、シャープネス|タイトル、詳細な説明、イベント リスナー、接着点、テキスト
|パス `<draw:path> `|位置、サイズ、ビュー ボックス、スタイル、レイヤー、Z-Index、ID、キャプション ID と変換、テキスト アンカー、テーブルの背景、描画終了位置、パス データ|タイトル、詳細な説明、イベント リスナー、グルー ポイント、テキスト

### フレーム ###
図面ドキュメントのフレームは、テキスト ボックス、画像、またはオブジェクトを含む長方形のコンテナーです。フレームは、等高線、画像マップ、ハイパーリンクなどの追加機能をサポートしています。フレームには、画像だけでなくオブジェクトも含めることができるため、オブジェクトの複数のレンディションを持つことができます。アプリケーションは、最適なサポートに基づいてそれぞれの要素をレンダリングします。

フレームには次のものを含めることができます。
* テキストボックス
* OpenDocument 形式またはオブジェクト固有のバイナリ形式で表されるオブジェクト
*画像
* アプレット
* プラグイン
*フローティングフレーム

フレームは、次のようにドキュメントに含まれます。

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## 参照 ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 形式 - ウィキペディア](https://en.wikipedia.org/wiki/OpenDocument)

