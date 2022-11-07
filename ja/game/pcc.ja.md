{
  "date" : "2021-09-08",
  "keywords" :[ "pcc ファイル", "pcc ファイル形式", "pcc ファイルとは", "ファイル", "pcc の例", "pcc ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Mass Effect PCC ファイル形式と,PCC ファイルを作成して開くことができる API について学びます。",
  "title" :"PCC - 質量効果パッケージ ファイル",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .PCC オプション番号

.pcc の付いたファイルは、モデル、テクスチャ、および部屋。 Mass Effect 2 および 3 は、Unreal Engine 3 ゲーム エンジンに基づく最初のシューティング ゲームです。このゲームは当初、[Bioware](https://www.bioware.com/about/) によって開発され、ゲーム リソースの大部分を独自の PCC ファイル形式で保持していました。 Bioware は、世界をリードするインタラクティブ エンターテイメント パブリッシャーである Electronic Arts に買収されました。

## PCC ファイル形式 - 詳細情報

PCC ファイルには、全体的なファイル構成に寄与する圧縮および/または非圧縮構造が含まれています。

### 圧縮 PCC 構造

圧縮された PCC ファイルは、チャンクに分割されたテーブルとデータで構成されます。各チャンクには、可変数の圧縮ブロックが含まれます。

* `Chunks Header` - チャンクに関する情報を含む 16 バイトの共通ヘッダー。
* `Chunk Header` - ブロック形式に含まれる生の圧縮データに関する情報を含む 16 バイトのヘッダー。

### 非圧縮 PCC 構造

圧縮されていない PCC ファイルは、次の 5 つの部分に分かれています。

* `Header` - PCC ファイルの構造に関する基本的な情報が含まれています。
* `Name Table` - インポート クラス、エクスポート、およびエクスポート プロパティを含む、パッケージ内にある名前が含まれます。
* `Import Table` - PCC によってインポートされたすべてのクラスとオブジェクトが含まれます。
* `Export Table` - パッケージに格納されているすべてのオブジェクトが含まれます。各エクスポートのサイズはさまざまです。

## 参考文献

* [Me3Explorer - PCC ファイル形式](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [マスエフェクトゲーム](https://www.ea.com/games/mass-effect/mass-effect-3)
* [バイオウェア](https://www.bioware.com/about/)

