{
  "date" : "2021-05-24",
  "keywords" :["xul", "ファイル", "拡張子", "ファイル形式", "ファイル拡張子", "XML ユーザー インターフェイス言語"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML ユーザー インターフェイス言語ファイル",
  "description":"XUL ファイル形式と,XUL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .XUL ファイルとは?

拡張子が .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) は XML User Interface Language の略) の付いたファイルは、[XML](/web/xml/) ベースのマークアップ言語ファイルです。ユーザー インターフェイスの作成。 Web ページの作成に使用される他のマークアップ言語と同様のグラフィカル ユーザー インターフェイス要素を開発者が作成するために、Mozilla によって開発されました。 XUL は、Mozilla コードベースを使用した Firefox ブラウザーで Mozilla によって広く使用されています。 XUL レンダリングは、
[Gecko エンジン](https://en.wikipedia.org/wiki/Gecko_(software))。 Pale Moon、Basilisk、Waterfox などの Firefox フォークは、XUL アドオンのサポートを維持します。 XUL ファイルは、MIME タイプ application/vnd.mozilla.xul+xml で識別されます。

## XUL ファイル形式

XUL ファイルは、XML ファイル形式に基づくプレーン テキストで記述され、Gecko エンジンを使用してレンダリングされます。 XUL 構造の 3 つの主要部分は次のとおりです。

* `Content` - これには、ウィンドウの宣言と、それらに含まれるユーザー インターフェイス要素が含まれます。
* `Skin` - スタイル シート、画像、その他のテーマ関連ファイルが含まれます。ウィンドウの外観は、スタイル シートに記述されています。
* `Locale` - ウィンドウ内に表示されるテキストは個別に保存され、ユーザーは複数の言語ファイル セットを使用できます。

### XUL の例

次の例では、垂直方向に積み重ねられた 3 つのボタンを作成します。

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## 参考文献

* [XUL - ウィキペディアによる](https://en.wikipedia.org/wiki/XUL)
* [XUL アーカイブ ドキュメント - Mozilla による](https://wiki.mozilla.org/XUL:Home_Page)

