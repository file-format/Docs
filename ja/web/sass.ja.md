---
date: 2019-10-11
keywords: sass, .sass, sass ファイル形式, sass ファイルの開き方, 構文的に素晴らしいスタイルシート, css プリプロセッサ, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass ファイル形式
linktitle: Sass
description: "Sass ファイル形式と,Sass ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## .SASSファイルとは? ##

Sass (構文的に優れたスタイル シート) は、プリプロセッサ スクリプト言語です。 [CSS](/web/css/) にコンパイルされ、.sass 拡張子で保存されます。 Sass は、.sass 拡張子を使用するインデントに基づく元の構文と、.scss 拡張子を使用する CSS のようなブロック形式の新しい SCSS の 2 つの構文で構成されます。

## Sass を使用する理由 ##

Sass は、スタイルの操作を楽しくする変数、ネスト、ミックスイン、インポート、セレクター継承などの多くの機能を提供するため、スタイルの維持に非常に役立ちます。

## SASS ファイルの使用方法 ##

SASS ファイルは、[HTML](/web/html/) ドキュメントに直接含まれるのではなく、HTML ファイルに含まれる CSS ファイルに変換されます。 [Official Sass Site](https://sass-lang.com/install) の指示に従って、システムの Sass をインストールできます。

Sass は、既に保存されている SASS ファイルを変換するか、ファイルの保存時に変更を監視して変換することにより、CSS に変換できます。両方のコマンドを以下に示します。

### 一度だけ変換 ###

コマンドの最初のパラメーターはソース SASS ファイルで、2 番目のパラメーターは出力 CSS ファイルです。

```cmd
sass main.sass main.css
```

### 変更に注意してください ###

上記のコマンドは、コマンドの実行を維持する追加の *watch* フラグを使用して実行でき、Sass ファイルが保存されるとすぐに出力 CSS が生成されます。

```cmd
sass --watch main.sass main.css
```

## Sass 構文 ##

Sass は、変数、ネスト、ミックスイン、インポート、セレクターの継承などをサポートしています。これらの機能の例を以下に示します。

### 変数 ###

変数を使用して、ボタンの原色やパディングなどの再利用可能な情報を設定できます。これは、将来その情報を変更する必要が生じた場合に役立ちます。1 つの場所で変更するだけで、すべての場所で更新されます。

**サス**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**生成された CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### ネスティング ###

CSS セレクターは、HTML の階層と同様にネストできます。次の例では、スパンは h1 ブロック内にネストされています。

**サス**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**生成された CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### ミックスイン ###

ミックスインは、複数の場所で使用される類似のプロパティをグループ化するために使用されます。ミックスインはパラメータもサポートしています。

**サス**

**ミックスインの宣言**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**ミックスインの使用**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**生成された CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

＃＃＃ 拡張する ＃＃＃

拡張/継承は、1 つのセレクターのプロパティを別のセレクターと共有する必要がある場合に役立ちます。以下の例では、*.error-notice* セレクターは *.error-text* セレクターのすべてのプロパティを取得し、border および padding プロパティを追加します。

**サス**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**生成された CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

＃＃＃ 輸入 ＃＃＃

インポートは、機能または従うその他の構造に基づいてスタイルを異なるファイルに構造化する場合に役立ちます。これらのファイルはすべて、後で CSS に変換されるプライマリ SASS ファイルにインポートできます。インポート時には、インポート命令でファイル拡張子を指定する必要はありません。 Sass はすべての SASS ファイルを直接コンパイルします。インポート ファイルが直接コンパイルされるのを避けるために、名前の先頭にアンダースコア (_) を追加してパーシャルにすることができます。パーシャルは、通常の Sass ファイルと同様にインポートされます。

**サス**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

出力 CSS には、インポートされたすべてのファイルのスタイルが含まれます。

## 参照 ##

- [サス - ウィキペディア](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [サス](https://sass-lang.com/)

