{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "ファイル形式", "pak ファイルとは", "ファイル", "pak の例", "ビデオ ゲーム パッケージ ファイル","拡張子"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":".pak ファイルと,PAK ファイルを作成して開くことができる API について学びます。",
  "title" :"PAK ファイル形式 - ビデオ ゲーム パッケージ ファイル",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## .PAK オプション番号

PAK ファイルは、さまざまなビデオ ゲームでゲーム データをアーカイブするために作成されたパッケージ ファイルです。基本的に、これはゲームのファイル形式です。これには、グラフィック、テクスチャ、サウンド、オブジェクトなどの複数のゲーム要素と、他のゲーム データを含めることができます。アーカイブはほとんどが .zip ファイルとして保存され、WinZip や WinRAR などの一般的な解凍ソフトウェアで解凍できます。 PAK ファイルを使用するビデオ ゲームの例には、Quake、Hexen、Crysis、Half-Life などがあります。

## PAK ファイル形式 - 詳細情報

ほとんどの場合、PAK ファイルは [ZIP ファイル形式](/compression/zip/) で保存されます。ただし、アプリケーションによっては、これらのファイルを保存するために異なるファイル形式を使用する場合があります。


## PAK ファイルを開くには?

[PakExplorer](https://www.quaketerminus.com/tools.shtml) や [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) などのアプリケーションで PAK ファイルを開くことができます。

**------------------------------------------------ -------------------------------------------------- -----------------------**

## PAK ファイル形式 - Simutrans オブジェクト ファイル

拡張子が .pak のファイルは、[Simutrans](https://www.simutrans.com/en/) 交通シミュレーション ゲーム ファイル形式です。ユーザーが作成したグラフィックやデータコンテンツなど、シミュレーションで使用されるオブジェクトが含まれています。ゲームの乗り物、建物、地形など、いくつかの異なるオブジェクトを持つことができます。PAK ファイルは、これらのシミュレーション オブジェクトを作成するための .dat ファイルと .png 画像をコンパイルするユーティリティである MakeObject を使用して生成されます。 Simutrans を使用すると、乗客、郵便物、商品の陸上輸送システムを構築および管理することで、プレイヤーは成功した輸送システムを実行できます。

## PAK ファイルの作成方法

Simutrans には、Windows および Linux OS で PAK ファイルを作成するためのサンプル例がリストされています。

### Windows OS

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## 参考文献

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

