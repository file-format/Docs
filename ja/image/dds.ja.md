{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS ファイル形式 - DirectDraw サーフェス イメージ ファイル",
  "description":"DDS ファイル形式と,DDS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## .DDS オプション番号

DDS ファイルは、DirectDraw Surface (DDS) コンテナー形式を利用するラスター イメージ ファイルです。非圧縮および圧縮 (DXTn) テクスチャを格納し、さまざまなタイプのデータを格納するためにさまざまなタイプを実装します。また、単一レイヤー テクスチャ、ミップマップを含むテクスチャ、キューブ マップ、ボリューム マップ、テクスチャ配列など、いくつかの異なるタイプのデータもサポートしています。これにより、DDS ファイルは、デジタル写真や Windows デスクトップの背景に加えて、ビデオ ゲームのテクスチャ ユニット モデルを保存できます。 DDS ファイル形式は、DirectX SDK で使用するために Microsoft によって開発されました。

## DDS ファイル形式

DDS ファイルはバイナリ ファイルとして保存され、DirectX SDK で使用できます。 DirectX の機能を利用して、3D ゲームなどのリアルタイム レンダリング アプリケーションを開発します。

### DDS ファイルのレイアウト

[DDS ファイル レイアウト](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) は、Microsoft によって詳細に文書化されています。バイナリ DDS ファイルには、次の情報が含まれています。

* 4 文字のコード値 'DDS' (0x20534444) を含む DWORD (マジック ナンバー)。
* ファイル内のデータの説明。

DDS_HEADER はデータを記述し、DDS_PIXELFORMAT はピクセル形式を記述します。これらは両方とも、非推奨の DDSURFACEDESC2、DDSCAPS2、および DDPIXELFORMAT DirectDraw 7 構造体を置き換えます。

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[DDS ファイル形式のプログラミング ガイド](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) では、このファイル形式の技術的な詳細がさらに詳しく説明されています。

## 参考文献

* [DDS - ウィキペディアによる](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX ファイル フォーマット テクニカル リファレンス マニュアル](http://qzx.com/pc-gpe/pcx.txt)

