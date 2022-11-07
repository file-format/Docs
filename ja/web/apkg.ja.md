{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg ファイル", "apkg ファイル形式", "apkg ファイルの種類", "ファイル", "種類", "APkg ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki フラッシュカード デッキ ファイル形式",
  "description" :"APCG ファイルとは何か,およびそれらを作成して開くことができる API について学びます。",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## APKGファイルとは何ですか?

拡張子が .apkg のファイルは、フラッシュカード ベースの学習プログラムである [Anki](https://ankiweb.net/about) ソフトウェア アプリケーションで使用するために生成されたフラッシュカードのデッキです。 Anki アプリケーションに読み込まれて表示される [HTML](/web/html/) テキストが含まれており、さらに視覚的および聴覚的な学習用の画像と音声を含めることができます。 Anki では、ユーザーが独自の Anki フラッシュカード デッキを作成したり、他のユーザーのフラッシュカード デッキをインポートしたりできます。

## APKGファイル形式

Anki カード デッキは、Web ページを作成するための有名で一般的な言語である HTML で記述されたテンプレートから作成されます。デッキ カードのスタイリングは、Web ページのスタイリングに使用される言語である CSS を使用して行われます。スタイリングには、次の変更が含まれます。

* font-family - カードで使用されるフォントの名前。
* font-size - フォントのサイズ (ピクセル単位)。
* text-align - テキストを中央、左、右のいずれに配置するかを定義します。
* color - テキストの色を定義します。「青」、「赤」などの単純な色名または HTML カラー コードを使用できます。
* background-color - カードの背景色を定義します

スタイル情報はすべてのカードで共有され、変更が加えられるとすべてのカードに影響します。次の例では、最初のカードを除くすべてのカードに黄色の背景を使用します。

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Anki カードでの画像のサイズ変更は、次のように制御できます。

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Anki カードに Javascript を埋め込む

カード テンプレートを使用して、[Javascript](/web/js/) を Anki カードに埋め込むことができます。ただし、Javascript は高度なレベルであるため、サポートは提供されていません。さらに、レンダリング デバイスは、カード内の Javascript の実装の影響を異なる方法で示す場合があり、その結果、すべてのデバイスで実装をテストする必要があります。 window.alert などの特定の Javascript 機能により、作成した Javascript コードのデバッグが困難になります。

## 参照 ##

* [Anki ドキュメント](https://docs.ankiweb.net/intro.html)

