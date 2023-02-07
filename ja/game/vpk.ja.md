{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"アンリアル スタティック メッシュ VPK ファイル フォーマットと,VPK ファイルを作成して開くことができる API について学びます。",
  "title" :"VPK ファイル - アンリアル スタティック メッシュ ファイル",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## .VPK オプション番号

.vpk ファイルは、Valve Corporation が開発したゲーム エンジンである **Source Engine** で使用されるファイル形式です。 VPK ファイルは、モデル、テクスチャ、サウンドなどのゲーム コンテンツをパッケージ化するために使用され、Team Fortress 2、Left 4 Dead、Counter-Strike: Global Offensive などのゲームで一般的に使用されます。ファイルは、GCFScape や VPK ツールなどのさまざまなツールを使用して開いたり抽出したりできます。

## VPK ファイル形式 - 詳細情報

VPK ファイルは、バイナリ ファイルとしてディスクに保存されます。単一の vpk ファイルは、VPK パッケージの一部にすることも、独立した生の VPK ファイルとして機能させることもできます。 VPK ファイル内に格納できる情報には、マップ、マテリアル、ゲーム コンテンツ、および振り付けシーンが含まれます。

### VPK ファイルの作成方法

使用可能なツールに応じて、.vpk ファイルを作成する方法がいくつかあります。

1. `VPK ツールの使用:` これは、VPK ファイルの作成と抽出に使用できるコマンドライン ツールです。 VPK ファイルは、次のコマンドを使用して作成できます。
```
"vpk.exe -M <directory> <output_file.vpk>"
```
これにより、指定されたディレクトリから VPK ファイルが作成され、指定された出力ファイルとして保存されます。

1. `Hammer Editor の使用:` Hammer Editor は、Source エンジンを使用するゲームのレベルを作成および編集するために使用できる Source SDK に含まれるツールです。また、[ファイル システム] タブでフォルダーを右クリックし、[VPK の作成] を選択して、VPK ファイルを作成する機能も含まれています。

1. `Valve の VPK クリエーターの使用:` これは、Valve が開発したツールで、ゲーム コンテンツのパッケージ化と配布に使用されます。このツールは、VPK ファイルの作成に使用でき、VPK ファイルを作成するための公式ツールでもあります。

## 参考文献

※【バルブソフト】(https://www.valvesoftware.com/ja/)
* [VPK 開発者リソース](https://developer.valvesoftware.com/wiki/GCF)

