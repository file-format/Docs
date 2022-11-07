{
  "date" : "2021-09-08",
  "keywords" :[ "mgx ファイル", "mgx ファイル形式", "mgx ファイルとは", "ファイル", "mgx の例", "mgx ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Age of Empires 2 Expansion Replay MGX ファイル形式と,MGX ファイルを作成して開くことができる API について学びます。",
  "title" :"MGX - エイジ オブ エンパイア 2 拡張リプレイ",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .MGX オプション番号

拡張子が .mgx のファイルは、Age of Empires II: The Conquerors ゲームの記録ファイルで、Age of Empires II プログラム内で再生できます。ユーザーがプレイしたキャンペーンの完全な記録が含まれています。 Age of Empires II プログラム内で読み込んで再生できます。リプレイすると、ユーザーがキャンペーンのために計画してプレイしたすべてのイベントとシナリオがゲームに表示されます。

## MGX ファイル形式 - 詳細情報

MGX ファイルの内部ファイル形式は、[Age of Empires 2: The Conquerors — Savegame File Format Specification] (https://github.com/stefan-kolb/aoc-mgx-フォーマット）。仕様では、次のセクションで詳細を概説します。

### 構造体の定義

GPX ファイル形式の構造定義は、構造化されたバイナリ データを読み書きする方法を提供する [BinData Ruby Gem 宣言](https://github.com/dmendel/bindata/wiki) に基づいていると考えられています。これにより、プログラマは BinData によって読み書きされるバイナリ データの形式を指定できます。

### MGX メッセージング

MGX メッセージングは、2 種類のメッセージに基づいています。

* GAMESTART - ゲーム開始コマンドを指定し、現在まで検証されていません
* CHAT - ゲーム内のチャット メッセージについて説明します。プレイヤーとゲーム自体 (Gaia) の両方がゲーム内メッセージを送信できます。

### ゲームプレイアクション

[GAMEPLAY アクション](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) がいくつか取得され、詳細が利用可能です。

## 参考文献

* [Age of Empires 2: The Conquerors — セーブゲーム ファイル形式の仕様](https://github.com/stefan-kolb/aoc-mgx-format)

