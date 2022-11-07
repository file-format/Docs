---
date: 2019-10-11
keywords: css,.css,css ファイル形式,css ファイルの開き方,カスケーディング スタイル シート
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS ファイル形式
linktitle: CSS
description: "CSS ファイルの形式と,CSS ファイルを作成して開くことができる API について説明します。"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## CSS ファイルとは何ですか? ##

CSS (カスケーディング スタイル シート) は、HTML 要素が画面や紙などにどのように表示されるかを記述したファイルです。HTML を使用すると、スタイルを埋め込んだり、外部スタイルシートでスタイルを定義したりできます。スタイルを埋め込むには、\ <style>\</style>タグが使用されています。外部スタイルシートは、拡張子が .css のファイルに保存されます。外部 CSS を使用すると、それを複数の HTML ページに含めて、それらのページのスタイルを更新できます。単一の CSS ファイルでも、完全な Web サイトのスタイルを設定するために使用できます。

## 簡単な歴史 ##

CSS1 は 1996 年に Bert Bos を共著者としてリリースされました。 CSS ワーキング グループは、CSS1 で扱われなかった問題に取り組み始めました。この結果、1997 年 11 月に CSS2 が作成され、1998 年 5 月 12 日に W3C 勧告として公開されました。このバージョンでは、プリンター、ダウンロード可能なフォント、テーブル、要素の配置など、メディア固有のデバイスのサポートが追加されました。 1999 年 6 月、CSS3 は W3C の推奨事項になりました。これにより、ドキュメントがモジュールに分割され、各モジュールには CSS2 で定義された拡張機能が含まれていました。

## CSSファイルの使い方##

CSS ファイルを使用するには、HTML ドキュメントの head セクションに含めます。以下に示すように、link タグを使用してファイルをインクルードします。

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

link タグの *href* 属性には、CSS ファイルへのパスが含まれています。これにより、同梱の CSS ファイルに含まれる適用可能なスタイルが HTML ドキュメントに適用されます。

## CSS 構文 ##

CSS ルールは、セレクターと宣言の 2 つのコンポーネントで構成されます。セレクターは、HTML ドキュメント内の要素を指します。要素タグ、クラス名、ID 名、階層を示す複数のタグなどのいずれかです。宣言には、プロパティと値で構成されるスタイル定義が含まれます。プロパティは、変更する要素のプロパティを識別し、値はその新しい値を定義します。各 CSS ルールには、複数の宣言を含めることができます。以下は、CSS ルールの例です。

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

上記の例では、HTML ドキュメント内のすべての h1 タグを選択するセレクターとして **h1** があります。この規則には、font-weight 用と color 用の 2 つの宣言があります。 *font-weight* と *color* はプロパティで、*700* と *forestgreen* はそれぞれの値です。

## CSS の使用例 ##

以下に、HTML ドキュメントの例と、スタイルを設定するために使用されるスタイルシートを示します。スタイル付きの HTML ドキュメントとプレーンな HTML ドキュメントを比較するために、比較画像も追加されます。

### HTML ドキュメント ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS スタイルシート ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### 出力比較 ###

画像の左側にはスタイルが適用されていない HTML ドキュメントが表示され、右側にはスタイルが適用された HTML ドキュメントが表示されます。

{{< figure src="../CssExample.jpg" alt="サンプル画像" >}}

## 参照 ##

- [CSS - ウィキペディア](https://en.wikipedia.org/wiki/CSS)

