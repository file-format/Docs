{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"GCF ファイル形式と,GCF ファイルを作成して開くことができる API について学びます。",
  "title" :"GCFファイル - ナデオゲームGCFフォーマット",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## .GCF オプション番号

.gcf ファイルは、Steam ゲーム プラットフォームで使用されるゲーム キャッシュ ファイルです。これには、ゲームで使用されるテクスチャ、モデル、その他のファイルなどのゲーム データが含まれます。これらのファイルはユーザーのコンピューターに保存され、ゲームの更新またはインストール時にダウンロードする必要があるデータの量を減らすために使用されます。 .gcf ファイルを使用して、ゲームのインストールのバックアップを作成したり、コンピューター間でゲームを転送したりすることもできます。

GCF ファイルは、オープン ソース C++ プログラミング ライブラリ [HLLib](https://developer.valvesoftware.com/wiki/HLLib) で読み書きできます。

## GCF ファイル形式

GCF ファイルはバイナリ ファイルとしてディスクに保存されます。 GCF は、もともと Grid Cache File (Steam の初期のコード名は Grid) の頭字語として使用されていましたが、後に Game Cache File として採用されました。 GCF ファイルは、Steam ゲームを保存するアーカイブ ファイルです。すべての公式コンテンツは GCF ファイルとしてダウンロードされます。 GCF ファイルは、ゲーム間で共有することもできます。

注: GCF は [VPK ファイル形式](/ja/game/vpk/) の前身です。
## 参考文献

* [バルブソフトウェア](https://www.valvesoftware.com/en/)
* [GCFファイル形式](https://developer.valvesoftware.com/wiki/GCF)
* [HLLib - GCF ファイルを読み取るためのオープン ソース C++ プログラミング ライブラリ](https://developer.valvesoftware.com/wiki/HLLib)

