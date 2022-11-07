---
date: 2019-10-11
keywords: scss, .scss, scss ファイル形式, scss ファイルの開き方, 構文的に素晴らしいスタイルシート, css プリプロセッサ, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS ファイル形式 - Sass カスケード スタイル シート
linktitle: SCSS
description: "SCSS ファイル形式と,SCSS ファイルを作成して開くことができる API について説明します。"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## .SCSS ファイルとは? ##

SCSS は、インデントの代わりにブラケットを使用する Sass (Syntactically Awesome Stylesheet) の 2 番目の構文です。 SCSS は、有効な CSS3 ファイルが有効な SCSS ファイルでもあるように設計されています。 SCSS ファイルは .scss 拡張子で保存されます。

## SCSS を使用する理由 ##

Web サイトのデザインが複雑になり、[CSS](/web/css/) ファイルが大きくなっています。このようなファイルは保守が困難です。ここで SCSS の出番です。SCSS は、CSS 開発における変数、ネスト、ミックスイン、インポート、およびセレクターの継承を導入します。これらの追加により、デザインの作業がより楽しくなります。

## SCSSファイルの使い方##

SCSS ファイルは、CSS のように [HTML](/web/html/) ドキュメントに直接含まれません。代わりに、SCSS ファイルは、HTML ファイルに含まれる CSS ファイルに変換されます。システムに SCSS をインストールするには、[Official Sass Site](https://sass-lang.com/install) の指示に従ってください。
SCSS を CSS に変換するには、既に保存されている SCSS ファイルを変換するか、ファイルの保存時に変更を監視して変換します。両方のコマンドを以下に示します。

### 一度だけ変換 ###

最初のパラメーターはソース SCSS ファイルで、2 番目のパラメーターは出力 CSS ファイルです。

```cmd
sass main.scss main.css
```

### 変更に注意してください ###

コマンドには、コマンドの実行を維持する追加の *watch** フラグがあり、SCSS ファイルが保存されるとすぐに出力 CSS が生成されます。

```cmd
sass --watch main.scss main.css
```

## SCSS 構文 ##

SCSS は、変数、ネスト、ミックスイン、インポート、セレクターの継承などをサポートしています。これらの機能の例を以下に示します。

### 変数 ###

変数を使用して、保存ボタンの原色や背景色などの再利用可能な情報を設定できます。これは、その情報を変更する必要がある場合に便利です。1 つの場所で変更するだけで、使用されている場所が更新されます。

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

HTML の階層と同様に、CSS セレクターをネストできます。以下の例では、スパンは h1 ブロック内にネストされています。

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

ミックスインを使用して、複数の場所で一緒に使用される類似のプロパティをグループ化できます。パラメータを mixin に渡すこともできます。

**SCSS**

**ミックスインの宣言**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**ミックスインの使用**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

拡張/継承は、あるセレクターのプロパティを別のセレクターと共有する必要がある場合に役立ちます。以下の例では、*.error-notice* セレクターは *.error-text* セレクターのすべてのプロパティを取得し、border および padding プロパティを追加します。

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

インポートは、懸念事項の分離に役立ちます。ヘッダー スタイルを別のファイルに、フッター スタイルを別のファイルに、スタイルで使用されるすべての色変数を別のファイルに、などのようにスタイルを分割できます。この手法を使用すると、スタイルは整理されたままです。以下の例に示すように、メインの SCSS ファイルにファイルをインポートするだけです。インポート命令でファイル拡張子を指定する必要はありません。 Sass はすべての SCSS ファイルを直接コンパイルします。インポート ファイルが直接コンパイルされるのを避けるために、名前の前にアンダースコア (_) を追加してパーシャルにすることができます。アンダースコアなしの通常の SCSS ファイルと同様のパーシャルをインポートできます。

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

出力 CSS には、インポートされたすべてのファイルのスタイルが含まれます。

## 参照 ##

- [SCSS - ウィキペディア](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [サス](https://sass-lang.com/)

