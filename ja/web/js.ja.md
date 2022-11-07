---
date: 2019-10-11
keywords: js, .js, js ファイル形式, js ファイルの開き方, javascript ファイル
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS ファイル形式
linktitle: JS
description: "JS ファイル形式と,JS ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## .JS ファイルとは何ですか? ##

JS (JavaScript) は、Web ページで実行するための JavaScript コードを含むファイルです。 JavaScript ファイルは .js 拡張子で保存されます。 [HTML](/web/html/) ドキュメント内に、\ を使用して JavaScript コードを埋め込むことができます。 <script>\</script>タグを付けるか、JS ファイルを含めます。 [CSS](/web/css/) ファイルと同様に、コードを再利用できるように、JS ファイルを複数の HTML ドキュメントに含めることができます。 JavaScript を使用して HTML DOM を操作できます。

## 簡単な歴史 ##

JavaScript は、1995 年 9 月に Navigator Browser の一部として、Netscape の LiveScript という名前で最初に出荷されました。 3 か月後に JavaScript に改名されました。 1996 年、Microsoft は Navigator のインタープリターをリバース エンジニアリングして JScript を作成しました。 JScript は Internet Explorer と共にリリースされ、JavaScript とは大きく異なっていました。

Netscape は、1997 年に最初の ECMAScript 仕様の公式リリースにつながる JavaScript を ECMA International に提出しました。

Jesse James Garrett は 2005 年にホワイト ペーパーを発表し、その中で *Ajax* という用語を作り出しました。これは、JavaScript をバックボーンとして使用して、バックグラウンドでデータをロードし、ページ全体のリロードを回避する Web アプリケーションを作成しました。これにより、JQuery、Prototype、Dojo などのライブラリが作成されました。

Google は 2008 年に V8 JavaScript エンジンを搭載した Chrome ブラウザをリリースしました。2009 年の初めに、関連するすべての作業を組み合わせて JavaScript を推進するための合意がなされました。これにより、2009 年 12 月に ECMAScript 5 標準がリリースされました。

## JSファイルの使い方 ##

JS ファイルを使用するには、それを HTML ドキュメントに含めます。以下に示すように、link タグを使用してファイルをインクルードします。

```html
<script src="site.js"></script>
```

*script* タグの *src* 属性には、JS ファイルへのパスが含まれています。これにより、JS 機能が HTML ドキュメントに追加されます。

## JS 構文 ##

JavaScript ファイルには、変数、演算子、関数、条件、ループ、配列、オブジェクトなどを含めることができます。以下に、JavaScript の構文の概要を簡単に示します。

- 各コマンドはセミコロン (;) で終了します。
- *var* キーワードを使用して変数を宣言します。
- 値を計算するための算術演算子 ( + - * / ) をサポートします。
- 1 行コメントは // で追加し、複数行コメントは /* と */ で囲みます。
- すべての識別子は大文字と小文字が区別されます。つまり、*modelNo* と *modelno* は 2 つの異なる変数です。
- 関数は *function* キーワードを使用して定義されます。
- 配列は、角括弧 [] を使用して定義できます。
- JS は、==、!=、>=、!== などの比較演算子をサポートしています。
- クラスは、*class* キーワードを使用して定義できます。

## JS の使用例 ##

JavaScript ファイルの簡単な使用例を以下に示します。

### HTML ドキュメント ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS コード ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## 参照 ##

- [JS - ウィキペディア](https://en.wikipedia.org/wiki/JavaScript)

