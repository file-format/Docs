{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya 組み込み言語","ファイル", "拡張子", "ファイル形式", "Maya 3D", "プログラミング ガイド" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya 組み込み言語ファイル形式",
  "description":"MEL ファイル形式と,MEL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## .MEL ファイルとは?

拡張子が .mel (Maya Embedded Language)のファイルは、グラフィカル インタフェースを作成するために Autodesk Maya で使用されるスクリプト言語です。 Maya のグラフィカル インタフェースに加えて、実行可能なスクリプトを使用して、グラフィカル要素の作成を自動化できます。 MEL を使用すると、プログラミングを学ばなくてもグラフィカル インターフェイスを作成できます。これは、反復タスクを高速化するマクロとカスタム アクションを作成することによって実現されます。これらの手順とスクリプトを使用すると、カスタム モデリング、アニメーション、ダイナミクス、およびタスク レンダリングを作成できます。 Autodesk Maya 2020 を使用して、EML ファイルの内容を開いて表示できます。

## MEL ファイル形式 - 詳細情報

開発者は、Maya のドキュメント セクションで、プログラマー向けの [リファレンス マニュアル](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)を利用できます。 MEL は、UINX に似たシェル スクリプト コマンドに基づいて、目的を達成します。スクリプト ベースのコマンドにより、従来のオブジェクト指向プログラミング (OOP) とは無関係になり、他の言語のようにデータ構造を使用したり、関数を呼び出したり、OOP を使用したりする必要がなくなります。

MEL の重要なポイントは次のとおりです。

「コメント」 - MEL のすべてのステートメントは、ブロックの最後であっても、セミコロン (;) で終了する必要があります。

`戻り値` - 値を返す式を記述しても、MEL で値が自動的に出力されません。代わりに、エラーが発生します。
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
「作成、編集、および削除のコマンド」 - 同じコマンドを使用して、モノの作成、モノの編集、または既存のものに関する情報の照会を行います。ただし、フラグは、コマンドの実行内容 (作成、編集、または照会) を制御します。

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`関数からの戻り値` - 関数構文は自動的に値を返します。コマンド構文を使用して戻り値を取得するには、コマンドを逆引用符で囲む必要があります。

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## 参考文献

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

