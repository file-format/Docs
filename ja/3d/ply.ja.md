{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "ファイル", "拡張子", "形式", "3Dファイル形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"PLY ファイル形式と,PLY ファイルを作成して開くことができる API について学びます。",
  "title" :"PLY - ポリゴン 3D ファイル形式",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .PLY ファイルとは何ですか?

PLY (Polygon File Format) は、ポリゴンのコレクションとして記述されたグラフィカル オブジェクトを格納する 3D ファイル形式を表します。このファイル形式の目的は、幅広いモデルで役立つように一般的でシンプルで使いやすいファイル タイプを確立することでした。 PLY ファイル形式は、ASCII 形式とバイナリ形式で提供され、コンパクトなストレージと迅速な保存と読み込みが可能です。このファイル形式は、3D ファイルの読み取りをサポートするさまざまなアプリケーションで使用されます。

PLY 形式のオブジェクトは、頂点、面、およびその他の要素のコレクションと、これらの要素に関連付けることができる色や法線方向などのプロパティによって記述されます。オブジェクトと共に格納できるその他のプロパティには、次のものがあります。

* 表面法線
* テクスチャ座標
*透明度
* 範囲データの信頼度
* ポリゴンの前面と背面のプロパティ

PLY 形式で表されるオブジェクトは、手動でデジタル化されたオブジェクト、モデリング アプリケーションからのポリゴン オブジェクト、範囲データ、マーチング キューブからの三角形、テレイン データ、ラジオシティ モデルなど、さまざまなソースの結果である可能性があります。

## 簡単な歴史

PLY フォーマットは、1990 年代に Greg Turk とスタンフォード グラフィックス ラボの他のメンバーによって開発されたため、スタンフォード トライアングル フォーマットとしても知られています。それ以来、ファイル形式のバージョンは 1.0 であり、それ以上の変更は行われていません。

## PLYファイル形式

単純な PLY オブジェクトは、オブジェクトを表現するための要素のコレクションで構成されます。これは、頂点の (x,y,z) トリプルのリストと、頂点のリストへの実際のインデックスである面のリストで構成されます。頂点と面は要素の 2 つの例であり、PLY ファイルの大部分はこれら 2 つの要素で構成されています。新しいプロパティを作成してオブジェクトの要素に追加することもできますが、これらの新しいプロパティに遭遇したときに古いプログラムが壊れないように追加する必要があります。このようなプロパティは、アプリケーションを読み取ることによっても破棄できます。さらに、この要素を使用して、新しい要素を作成したり、プロパティを定義したりすることもできます。

### ファイル構造

PLY ファイル形式のファイル構造は次のとおりです。

|フィールド
---|
|ファイル ヘッダー
|頂点リスト
|フェイスリスト
|その他の要素のリスト

#### 構造例

PLY ファイル形式のさまざまな部分についての以降の説明では、次の例を使用します。

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### ファイル ヘッダー

PLY ファイル形式のヘッダーは、ASCII 形式とバイナリ形式の両方の ASCII テキストで構成されます。ヘッダー セクションの開始と終了は、 ply および end-header キーワードで識別されます。ヘッダーの先頭には、リーダーが PLY ファイル形式を認識するために使用されるマジック ワード ply があります。次の行は、このファイルのバージョン番号を示しています。 PLY ファイル形式のコメントは、各コメント行の先頭にあるコメント キーワードで始まります。

#### 要素キーワード

element キーワードは、ファイルの内容を示します。その後に、特定の要素タイプのプロパティが続きます。各プロパティには、以下に示すように、プロパティ タイプと順序が指定されています。

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

この特定の例では、特定の頂点要素に float 型の 3 つのプロパティがあり、その順序が指定されています。

#### データ型の種類

プロパティが持つことができるデータ型には 2 つのタイプがあります。

`Scalar`: スカラー データ型は次のとおりです。

|#Name|#Type|#バイト数
|文字|文字|1
|uchar|符号のない文字|1
|短い|短い整数|2
|ushort|符号なし短整数|2
|整数|整数|4
|uint|符号なし整数|4
|浮動小数点数|単精度浮動小数点数|4
|double|倍精度浮動小数点数|8

`List`: リスト データ型を使用する特別な形式のプロパティ定義があります。この例は、上記のキューブ ファイルからのものです。

`プロパティ リスト uchar int vertex_index`

これは、プロパティ "vertex_index" には、最初にプロパティに含まれるインデックスの数を示す符号なし char が含まれ、その後にその数の整数を含むリストが続くことを意味します。この可変長リストの各整数は、頂点へのインデックスです。

## 参照 ##

* [PLY ファイル形式](http://paulbourke.net/dataformats/ply/)
* [PLY - ウィキペディアによる](https://en.wikipedia.org/wiki/PLY_(file_format))

