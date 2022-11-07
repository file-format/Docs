{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "ファイル", "フォーマット", "開く", "読み取り", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD 設計ファイル形式",
  "description" :"DGN ファイル形式と,DGN ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## .DGN ファイルとは何ですか?

拡張子が .dgn (デザイン) のファイルは、MicroStation や Intergraph Interactive Graphics Design System などの CAD アプリケーションによって作成およびサポートされている図面ファイルです。高速道路、橋、建物などの建設プロジェクトの設計を作成および保存するために使用されます。このフォーマットは、Autodesk の [DWG](/cad/dwg/) ファイル フォーマットに似ており、競合他社と見なされています。 DNG ファイルは、Intergraph 標準ファイル形式または V8 DGN として保存できます。 DGN は、DWG、[BMP](/image/bmp/)、[JPEG](/image/jpeg/)、[PDF](/pdf/)、[GIF](/image/) など、他のいくつかの形式に変換できます。 gif/) など。 Corel PaintShop Photo Pro や IMSI TurboCAD Deluxe バージョンなどの他のソフトウェア アプリケーションに加えて、Autodesk AutoCAD、Bentley View、Bentley Systems MicroStation で開くことができます。

## V8 DGN ファイル形式

MicroStation V8 DGN ファイルは、1 つまたは複数のモデルで構成されています。モデルは要素のコンテナです。 V8 DGN は、以前のバージョンの MicroStation に存在していたファイル形式ベースの制約をすべて取り除きます。以下は、DGN ファイル形式の改良点のリストです。

* DGN ファイルのレベル数の制限がなくなり、各レベルに名前が付けられ、要素として保存されます。
* DGN ファイルの最大物理サイズには制限がなく、オペレーティング システムによってのみ制限されます (NT の制限は 4 GB など)。
※1要素の最大サイズは128KBです。
* セルの最大サイズに制限はありません。
※セル名は500文字程度までです。
* DGN ファイルに添付できる参照の数に制限はありません。
* ライン ストリング、シェイプ、またはポイント カーブは、最大 5000 個の頂点を持つことができます。
* 複雑なチェーンや複雑な形状のコンポーネントの数に制限はありません。
* DGN ファイル内のグラフィック グループの数に制限はありません。
*フェンスは、それが配置されているビューに対して平行です。
* 1 行のテキストには 65,535 文字を含めることができます。
* テキスト ノードの最大サイズに制限はありません。
* DGN ファイル内のテキスト ノードの数に制限はありません。
* 各要素には、要素のライフサイクルを通じて変化しない一意の 64 ビット識別子があります。
* 各要素には、最新の変更時刻を示すタイム スタンプがあります。

## 参考文献

* [DNG - ウィキペディアによる](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [MicroStation V8 DGN ファイル形式](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

