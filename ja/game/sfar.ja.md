{
  "date" : "2021-10-20",
  "keywords" :[ "sfar ファイル", "sfar ファイル形式", "sfar ファイルとは", "ファイル", "sfar の例", "Mass Effect 3 DLC ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Mass Effect 3 SFAR ファイル形式と,SFAR ファイルを作成して開くことができる API について学びます。",
  "title" :"SFAR - Mass Effect 3 DLC ファイル",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .SFAR オプション番号

拡張子が .sfar のファイルは、Mass Effect 3 が DLC (ダウンロード可能なコンテンツ) を圧縮された独自のアーカイブに保存するために使用するゲーム データ ファイルです。 Mass Effect 3 は、一流のゲーム開発会社である Electronic Arts によって作成されたゲームです。 SFAR ファイルに保存された DLC コンテンツは、追加のコンテンツと機能でゲームを拡張するために使用されます。

## SFAR ファイル形式 - 詳細情報

SFAR ファイルは、バイナリ ファイル形式の圧縮アーカイブ ファイルとして格納/保存されます。これらはコンテンツの圧縮に LZX と LZMA の両方の圧縮アルゴリズムを使用します。 SFAR ファイルは、ME3 Explorer に同梱されている DLC Editor を使用して開くことができます。 SFAR に加えて、DLC Editor は [PCC](/game/pcc/) などの他のゲーム ファイルを抽出できます。

## SFAR ファイル形式の仕様

SFAR ファイルは、次の 4 つの主要なチャンクに分割されます。

### SFAR ヘッダー

SFF ヘッダーには、ファイルを構成するさまざまなチャンクに関する情報が含まれています。

### SFAR ファイル テーブル

SFAR ファイル テーブルには、各エントリの長さが 30 バイトのファイル エントリのリストが含まれています。

### ブロックサイズ表

Block-Size には複数のエントリが含まれており、各エントリの長さは 2 バイトです。この値は、ファイル テーブルのエントリに対応するブロック サイズを指定します。

### ブロック

SFAR ファイル内のブロック チャンクには、SFAR ファイル内のデータが含まれます。

## 参考文献

* [DLC SFAR ファイル形式 - 研究](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

