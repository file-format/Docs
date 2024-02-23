
{
  "date": "2023-01-05",
  "keywords": [
"ハメ撮りファイル",
"pov ファイル形式",
"povファイルとは何ですか",
"ファイル",
"ハメ撮りの例",
"povファイル拡張子",
"拡大",
"フォーマット"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "POV ファイル形式と、POV ファイルを開いて作成できる API について学びます。",
  "title": "POV - ビジョンファイルの永続化",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-jav"
}
},
  "lastmod": "2023-01-05"
}

## POVファイルとは何ですか?

POV ファイルは、POV-Ray レイ トレーシング ソフトウェアの命令を含むプレーン テキスト ファイルです。これらの命令は、POV-Ray に固有の特別なスクリプト言語で書かれています。 3D オブジェクト、マテリアル、照明、シーンの外観を定義するその他のプロパティなど、レンダリングするシーンを指定します。 POV ファイルは、POV-Ray に固有の特別なスクリプト言語を使用しており、複雑で詳細な 3D シーンの作成に使用できます。 POV ファイルのファイル拡張子は通常、「.pov」または「.povray」です。 POV-Ray で POV ファイルを開くと、ソフトウェアはファイル内の命令を読み取り、それを使用してシーンのレンダリング イメージを生成します。

.pov ファイルは、映画、テレビ、ビデオ ゲーム、マーケティング資料など、さまざまなアプリケーション用の 3D グラフィックスやアニメーションを作成するためにアーティストやデザイナーによってよく使用されます。

## POV ファイル形式

**.pov ファイル**は通常、一連の **#include** ステートメントで始まります。これらのステートメントは、シーンで使用できる事前定義された色、テクスチャ、およびその他のリソースのライブラリを含めるために使用されます。次に、ファイルは一連のブロックを使用してシーンのオブジェクト、マテリアル、その他のプロパティを定義します。 .pov ファイルには他にも多くのタイプのオブジェクト、マテリアル、その他のプロパティを指定でき、ループや条件ステートメントを使用して、より複雑で詳細なシーンを作成できます。

## POV用ソフトウェアアプリケーション

.pov ファイル形式は POV-Ray レイ トレーシング ソフトウェアで使用されるため、.pov ファイルを開くための主なアプリケーションは POV-Ray ソフトウェア自体です。 POV-Ray の最新バージョンは、公式 Web サイト (https://www.povray.org/) からダウンロードできます。

POV-Ray に加えて、.pov ファイルを開いて編集できる次のようなアプリケーションが他にも多数あります。

- BRL-CAD: .pov ファイルをインポートおよびエクスポートできるオープンソース 3D モデリング ソフトウェア
- MeshLab: .pov ファイルをインポートおよびエクスポートできる 3D メッシュ処理ソフトウェア
- Blender: .pov ファイルをインポートおよびエクスポートできる人気のあるオープンソース 3D グラフィック ソフトウェア

.pov ファイルを開くことができる他のソフトウェア アプリケーションも存在する可能性があるため、上記のアプリケーションで .pov ファイルを開くことができない場合は、ファイル ビューアまたはコンバータ ツールを使用してみてください。

## POVの例

たとえば、以下は 1 つの青い円柱を持つシーンを定義するサンプル .pov ファイルです。

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

この例では、カメラ ブロックはシーン内のカメラの位置と方向を指定し、`light_source` ブロックは光源を宣言してその位置と色を指定し、`cylinder` ブロックは円柱オブジェクトを宣言してその端点を指定します。半径と材料特性。 POV-Ray ソフトウェアでこの .pov ファイルを開くと、単一の青い円柱の画像がレンダリングされます。

## 参考文献
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [ドキュメントPOV-Rayウェブサイト](http://www.povray.org/documentation/)

