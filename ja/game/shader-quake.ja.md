{
"日付":"2023-10-11",
   "keywords":[
"シェーダー",
"シェーダーファイル",
"シェーダー クエイク 3 エンジン シェーダー ファイル",
"シェーダーファイルを開く方法",
"ファイル",
"シェーダーファイル拡張子",
"拡大",
"ファイル"
],
   "author":{
"display_name":"シャキール・ファイズ"
},
"draft": "false",
"toc": true,
"title":"SHADER ファイル形式 - Quake 3 エンジン シェーダー ファイル",
   "description":"SHADER Quake 3 Engine Shader ファイル形式と,SHADER ファイルを作成して開くことができる API について学びます。",
"linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
"parent": "game"
}
},
"lastmod":"2023-10-11"
}

## SHADERファイルとは何ですか?

SHADER ファイル形式は、ゲーム内のテクスチャとマテリアルのシェーダを定義するために **Quake 3 エンジン** で使用されます。シェーダは、外観、反射率、透明度、その他の視覚的プロパティなど、サーフェスをレンダリングする方法を指定するために使用されます。

## Quake 3 エンジン SHADER ファイル

以下は、Quake 3 エンジン シェーダー ファイルの構造と構文の基本的な概要です。

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

Quake 3 エンジン シェーダ ファイルでは、それぞれが独自のプロパティとステージのセットを持つ複数のシェーダを定義できます。これらのシェーダは、ゲーム世界のさまざまなテクスチャやマテリアルの外観を定義するために使用されます。エンジンはこの情報を使用して、指定された視覚効果と動作でサーフェスをレンダリングします。

Quake 3 エンジンのシェーダー ファイルは、テクスチャとマテリアルがゲーム内でどのように表示されるべきかについての指示を含む単純なテキスト ファイルです。これらのファイルは通常のテキスト エディタで開いて編集でき、通常はゲームの .PK3 パッケージ内の **"/scripts"** ディレクトリにあります。

## クエイク 3 エンジン

Quake 3 エンジンは、id Software が開発した非常に影響力があり、多用途なゲーム エンジンです。 1999 年のゲーム「Quake III Arena」のリリースで初めて導入され、それ以来他のさまざまなゲームで使用されています。このエンジンは、高度なグラフィックス、マルチプレイヤー機能、および変更可能性で知られています。

Quake 3 エンジンの主な機能と側面をいくつか紹介します。

1. **グラフィック エンジン:** Quake 3 エンジンは、当時最先端のグラフィック テクノロジで知られていました。 1990 年代後半には画期的だった、曲面、シェーダー、ダイナミック ライティングなどの高度な機能が導入されました。
    





2. **マルチプレイヤー重視:** Quake 3 Arena は主にマルチプレイヤーの一人称シューティング ゲームとして設計されました。このエンジンのネットワーキング コードとオンライン マルチプレイヤー ゲームのサポートは優れており、競争力のあるオンライン プレイに人気の選択肢となっています。
    





3. **変更可能性:** Quake 3 エンジンは、変更可能であることで知られています。 id Software は、オープンソースの GNU General Public License (GPL) に基づいてエンジンのソース コードをリリースしました。これにより、多数の MOD やカスタム マップの作成が促進され、活気のある MOD コミュニティが形成されました。
    





4. **スクリプト化されたゲームプレイ:** エンジンはスクリプトベースのシステムを使用してゲームのルールと動作を定義し、モッダーやマッパーがカスタム ゲーム モードやユニークなエクスペリエンスを作成することを比較的簡単にしました。
    





5. **カスタム コンテンツのサポート:** Quake 3 のエンジンは、テクスチャ、モデル、サウンド ファイルなどのカスタム コンテンツをサポートしており、ユーザーが作成したマップや MOD で高度なカスタマイズが可能でした。
    





6. **レベル デザイン:** エンジンはブラシベースのレベル デザイン システムを使用しており、ソリッド ブラシから空間を切り出すことによってマップが構築されます。このアプローチは十分に文書化されており、レベル デザイナーにとって使いやすいものでした。


Quake 3 エンジンは、長年にわたって、「Return to Castle Wolfenstein」、「Star Wars Jedi Knight II: Jedi Outcast」、「Urban Terror」など、他の多くのゲームや MOD の基礎として使用されてきました。これはゲーム開発の世界に永続的な遺産を残し、一人称シューティング ゲームのジャンルの形成に貢献しました。その後、より新しく、より高度なエンジンが登場しましたが、Quake 3 エンジンはゲーム業界への貢献で引き続き尊敬されています。

## SHADERファイルを開くにはどうすればよいですか?

SHADER ファイルを開いたり参照したりするプログラムには次のものがあります。

- **id Software Quake 3** (有料) (Windows、Mac、Linux)
- Microsoft メモ帳
- メモ帳++
- 任意のテキストエディタ

## その他の SHADER ファイル

**.shader** ファイル拡張子を使用する他のファイル タイプは次のとおりです。

**ゲーム ファイル**
- [SHADER - Godot エンジン シェーダー ファイル](/ja/game/shader-godot/)
- [SHADER - Quake 3 エンジン シェーダー ファイル](/ja/game/shader-quake/)
- [SHADER - Unity シェーダー アセット](/ja/game/shader-unity/)

## 参考文献
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

