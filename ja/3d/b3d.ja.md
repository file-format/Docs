{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"B3D ファイル形式について学びます。blitz3d ゲームで使用され,B3D ファイルを開いて作成できる API です。",
  "title" :"B3D - Blitz3Dエンティティモデルファイル",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## B3D ファイルとは?

拡張子が .b3d のファイルは、Blitz3D で使用されるモデル ファイルで、キャラクター、建物、地形、その他のオブジェクトのビデオ ゲーム モデルが含まれている場合があります。 Blitz3D は、**blitz3d ゲーム**の作成に使用されるプログラミング言語です。 Blitz3D は、ビデオ ゲームを作成することのみを目的として設計された、強力で柔軟で使いやすいプログラミング言語です。開発者は、Blitz3D を使用するだけで、アクション満載の 3D ゲーム、2D パズル、アドベンチャー、RPG などを作成できます。

Blitz3D は BASIC プログラミング言語に基づいています。これは、習得も使用も簡単です。これらすべての事実により、Blitz は初心者にも経験豊富なプログラマーにも理想的なものになっています。その機能は、ほとんどの最新の 3D エンジンに見られるものよりもやや時代遅れと見なされていますが、Blitz3D は世界中の多くのゲーム プログラマーによって引き続き使用されています。

## Blitz3D の歴史

Blitz3D は基本的に、2001 年 9 月に Microsoft Windows オペレーティング システム用にリリースされ、他の同様のゲーム開発言語と競合しました。 Blitz3D は、以前の 2D エンジン BlitzBasic のアップグレード バージョンであり、DirectX 7 ベースの 3D エンジン用の API を追加してコマンド セットを拡張しました。 Blitz3D ユーザーは、BlitzBasic の後のエンジンである BlitzMax も比較する必要があります。 BlitzMax は、オブジェクト指向プログラミング言語をサポートする Blitz3D の複雑ですが、より強力なバージョンです。これは、Unicode 文字、OpenGL、および Windows だけでなく OSX および Linux へのエクスポートにより適した更新されたグラフィックス API です。

## B3D の例
1 つの TEXS チャンク、1 つの BRUS チャンク、および 1 つの NODE チャンクを含む b3d ファイルは、次のようになります。

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
シンプルで、アニメーション化もテクスチャもされていないメッシュは次のようになります。

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## 参考文献
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [ブリッツ BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

