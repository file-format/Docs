{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"MCR ファイル形式と,MCR ファイルを作成して開くことができる API について学びます。",
  "title" :"MCR - Minecraft 地域ファイル形式",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## .MCR オプション番号

Minecraft MCR ファイル形式は、Minecraft ワールドの地形チャンクを格納するために Minecraft で使用されるデータ形式です。これは、人気のオープンソース ゲーム エンジン Minecraft Forge の開発者によって開発された NBT (Named Binary Tag) 形式に基づいています。 MCR ファイル タイプは最初に導入され、後に [MCA ファイル形式](/ja/game/mca/) に置き換えられました。

## MCR ファイル形式

MCR ファイル形式は一連の名前付きバイナリ タグとして構造化されており、各タグには特定の種類のデータが含まれています。最上位のタグは「Level」タグで、1 つのゲーム レベルのすべてのデータが含まれています。 Level タグ内には、ゲーム ワールドに関する情報を格納する「Data」タグや、ゲーム ワールドに関するデータを格納する「Entities」および「TileEntities」タグなど、さまざまな種類のデータを格納する名前付きタグがいくつかあります。それぞれ、ワールド内のゲーム オブジェクトとタイル エンティティ。

## MCR ファイル形式の中身は何ですか?

Minecraft MCR ファイル形式では、リージョンはゲーム世界の 32x32 のブロック領域です。 MCR 形式は、データをより効率的に管理し、ゲーム レベルの読み込みと保存を高速化するために、ゲーム ワールドを領域に分割します。各地域は個別のファイルに保存され、MCR ファイル形式は座標系を使用して、ゲーム ワールド内の各地域の位置を識別します。領域の座標は、領域の左下隅のブロック座標によって決定されます。たとえば、座標が (-1,0) の領域は、ゲーム ワールドの原点から 1 領域左に配置され、0 領域下に配置されます。

## MCR ファイル形式の仕様

MCR ファイル形式の仕様は公開されています。 MCR 形式の基になっている NBT 形式の仕様は、Minecraft Forge の Web サイトで入手できます。さらに、[Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) にも MCR ファイル形式に関する詳細情報があり、その構造やサポートされているさまざまなデータ タイプが含まれています。

### MCR ファイルの圧縮データ

Minecraft MCR ファイル形式は圧縮をサポートしています。 MCR ファイル形式は、データを圧縮形式で保存できる [NBT 形式](https://minecraft.fandom.com/wiki/NBT_format) に基づいています。これにより、MCR ファイルのサイズが縮小され、転送と保存がより効率的になります。これは MCR ファイル形式の重要な機能であり、プレイヤーは大規模な Minecraft ワールドの地形データを他のユーザーと共有できます。

## 参考文献

* [Minecraft のワールド エディター](https://www.mcedit.net/)
* [マインクラフトについて](https://www.minecraft.net/)
* [地域ファイル形式](https://minecraft.fandom.com/wiki/Region_file_format)
* [NBT形式](https://minecraft.fandom.com/wiki/NBT_format)

