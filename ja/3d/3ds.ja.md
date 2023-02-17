{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","ファイル","形式","ファイルの種類","拡張子","3DSファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"3DS ファイル形式と,3DS ファイルを開いて作成できる API について学びます。",
  "title" :"3DSファイル形式",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 3DSファイルとは？

拡張子が .3ds のファイルは、Autodesk 3D Studio で使用される 3D Sudio (DOS) メッシュ ファイル形式を表します。 Autodesk 3D Studio は 1990 年代から 3D ファイル形式の市場にあり、現在では 3D モデリング、アニメーション、およびレンダリングを扱う 3D Studio MAX に進化しています。 3DS ファイルには、シーンや画像を 3D で表現するためのデータが含まれており、3D データのインポートおよびエクスポート用の一般的なファイル形式の 1 つです。カメラ位置、メッシュ データ、ライティング情報、ビューポート構成、スムージング グループ データ、ビットマップ参照、属性などの情報を考慮して、シーンをレンダリングするための頂点とポリゴンを作成します。

## 3DS ファイル形式 - 詳細情報
基本的に、3DS はバイナリ ファイル形式であり、データの保存と取得のために定義済みの構造に従います。バイナリ ファイル形式により、3DS ファイル形式は、テキスト ベースのファイル形式と比較して、より高速で小さくなります。 3DS ファイル内のデータは、チャンクの形式で保存されます。

### 3DSチャンク

3DS ファイルの各チャンクは、ID、次のブロックの位置を示すブロックの長さ、およびデータ自体を含むデータのブロックです。チャンク ID により、3DS ファイル形式リーダーは認識できないブロックをスキップできます。また、フォーマットの拡張性にも役立ちます。各チャンクには、一緒にシーンをレンダリングする形状、照明、表示情報に関連する情報が格納されます。チャンクは 3DS ファイル内で階層構造に配置され、表現は XML ドキュメント オブジェクト ツリーに似ています。

**チャンク ID:** チャンクの最初の 2 バイトは、ファイル リーダーが読み取り中にそれを考慮するかスキップするかを決定できるようにするチャンク ID を表します。

**チャンクの長さ:** チャンク ID の後に、チャンクの長さを表す 4 バイトの整数 (リトルエンディアン) が続きます。この長さには、データの長さ、そのサブブロックの長さ、および 6 バイトのヘッダーも含まれます。

**ペイロード:** チャンクの長さの後に、チャンクのデータの実際のバイトが続き、その後に同じ階層構造内のサブチャンクが続きます。このサブチャンクは、数レベルの深さまで拡張できます。

### チャンクの構造

単純なチャンクの階層構造は次のとおりです。

**チャンク**

|開始|終了|サイズ|名前
--- | --- | --- | ---
|0|1|2|チャンク ID
|2|5|4|次のチャンク

チャンクには、その ID によって識別される階層が適用されます。 3ds ファイルのプライマリ チャンク ID は 4D4Dh です。これは常にファイルの最初のチャンクです。プライマリ チャンクにはメイン チャンクがあります。

**メインチャンク**

|ID|説明
--- | ---
|3D3D|オブジェクト メッシュ データの開始。
|B000|キーフレーマー データの開始。

ID ブロックの後の次のチャンク ポインターは、次のメイン チャンクを指します。
Main チャンクの直後に別のチャンクがあります。これは、メイン チャンク スコープ内で許容される他のタイプのチャンクである可能性があります。
メッシュ記述 (3D3D) の場合、それらは任意の倍数になります。

**3D3D のサブチャンク - メッシュ ブロック**


|ID|説明
--- | ---
|1100|不明
|1200|背景色。
|1201|不明
|1300|不明
|1400|不明
|1420|不明
|1450|不明
|1500|不明
|2100|アンビエント カラー ブロック
|2200|霧?
|2201|霧?
|2210|霧?
|2300|不明
|3000|不明
|4000|オブジェクト ブロック
|7001|不明
|AFFF|不明

**4000 のサブチャンク - オブジェクト記述ブロック**
サブチャンク 4000 の最初の項目は、オブジェクト名の ASCIIZ 文字列です。
オブジェクトは、メッシュ、ライト、カメラのいずれでもかまいません。

|ID|説明
--- | ---
|4010|不明
|4012|影？
|4100|三角ポリゴン オブジェクト
|4600|ライト
|4700|カメラ

## 参考文献

* [ジオメトリ ファイル形式 - オートデスク](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS - ウィキペディアによる](https://en.wikipedia.org/wiki/.3ds)
