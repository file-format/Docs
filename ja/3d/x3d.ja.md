{
  "date" : "2019-10-11",
  "keywords" :[ "x3d ファイル", "x3d ファイル形式", "x3d ファイルとは", "ファイル", "x3d の例", "x3d ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D 画像ファイル",
  "description":"X3D ファイルを開いたり作成したりできる X3D ファイル形式と API について学びます。",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## X3D ファイルとは?
X3D は、3D 情報を表示するための [XML](/web/xml/) ベースの 3D グラフィックス ファイル形式です。これはモジュラー規格であり、いくつかの ISO 仕様によって定義されています。この形式は、ベクター グラフィックとラスター グラフィック、透明度、照明効果、および回転、フェード、スイングなどのアニメーション設定をサポートしています。 2001 年に [VRML](/3d/vrml/) ファイル形式の後継となりました。 3Dプリンタ。この形式は VRML への拡張機能を備えており、XML 構文だけでなく、VRML97 またはバイナリ形式の Open Inventor に似た構文を使用してシーンをエンコードする機能を提供します。

X3D の抽象仕様 (ISO/IEC 19775) は、2004 年に ISO によって最初に承認されました。X3D の XML および ClassicVRML エンコーディング (ISO/IEC 19776) は、2005 年に最初に承認されました。

## X3D ファイル形式

X3D シーン ファイルには、共通のファイル構造があります。

* ファイル ヘッダー (XML、ClassicVRML、または圧縮バイナリのいずれか)
* バージョンおよびプロファイル属性を含む X3D ルート ノードの開始
* Component ステートメントと Meta ステートメントを含む head セクション (どちらもオプション)
* X3D シーン グラフとその子ノード
* X3D ルート ノードの終わり

## X3D ファイル形式の例

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## 参照 ##

* [X3D - ウィキペディアによる](https://en.wikipedia.org/wiki/X3D)
※【Web3Dコンソーシアム公式サイト】(http://www.web3d.org/)
※【X3D公式サイト】(http://www.web3d.org/x3d/what-x3d)

