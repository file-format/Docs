{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf ファイル", "amf ファイル形式", "ファイル形式", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AMF ファイル形式と,AMF ファイルを開いて作成できる API について学びます。",
  "title" :"AMF - アディティブ マニュファクチャリング ファイル",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .AMF オプション番号
AMF ファイルは、アディティブ マニュファクチャリング プロセスで使用するためのオブジェクト記述のガイドラインで構成されています。開口部が含まれています<amf>XML タグであり、</amf>エレメント。この前に、ファイルの XML バージョンとエンコーディングを指定する XML 宣言行があります。宣言には測定単位の情報を含めることができ、そのような情報がない場合は、ミリメートルがデフォルトの単位として使用されます。


## AMF ファイル形式

アディティブ マニュファクチャリング ファイル形式 (**AMF**) は、3D プリントなどのアディティブ マニュファクチャリング プロセスで利用するために、オブジェクト記述のオープン スタンダードを定義します。 CAD プログラムは、オブジェクトの形状、色、素材などの情報を利用して、AMF ファイル形式を使用します。 AMF は、ラテラルが色、マテリアル、格子、および星座をサポートしていないため、STL 形式とは異なります。

### AMF ファイルの要素

で定義された 5 つの最上位要素<AMF>タグは以下のとおりです。完全に機能する AMF ファイルには、単一の object 要素が存在する必要があります。

`<object> ` - object 要素は、1 つまたは複数の素材のボリュームを定義し、それぞれが印刷用の素材 ID に関連付けられています。ファイルには少なくとも 1 つの object 要素が存在する必要があります。追加のオブジェクトはオプションです。

`<material> ` - オプションの material 要素は、関連付けられたマテリアル ID を持つ印刷用の 1 つ以上のマテリアルを定義します。 material 要素が含まれていない場合は、単一の既定の material が想定されます。

`<texture> ` - オプションの texture 要素は、それぞれに関連付けられたテクスチャ ID を持つ、色またはテクスチャ マッピング用の 1 つまたは複数の画像またはテクスチャを定義します。

`<constellation> ` - オプションの constellation 要素は、オブジェクトとその他の星座を印刷用の相対的なパターンに階層的に結合します。

`<metadata> ` - オプションのメタデータ要素は、ファイルに含まれるオブジェクトと要素に関する追加情報を指定します。

## AMF の例

以下は、[text](/word-processing/txt/) ファイルにコピーし、圧縮された [zip](/compression/zip/) ファイルとして保存して開くことができる AMF ファイルの例です。
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## 参考文献

* [AMF - ウィキペディア](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [ISO 上の AMF 仕様](https://www.iso.org/standard/67472.html)

