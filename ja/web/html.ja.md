{
  "date" : "2019-10-11",
  "keywords" :[ "html","html ファイル", "html ファイル形式", "html ファイルの種類", "ファイル", "種類", "html ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTMLファイル形式",
  "description":"HTML ファイル形式と,HTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .HTML ファイルとは?

HTML (ハイパー テキスト マークアップ言語) は、ブラウザーで表示するために作成された Web ページの拡張機能です。 Web の言語として知られる HTML は、Web ページの一部として表示される新しい情報要件の要件とともに進化してきました。最新のバリアントは HTML 5 として知られており、この言語での作業に多くの柔軟性を提供します。 HTML ページは、これらがホストされているサーバーから受信するか、ローカル システムからも読み込むことができます。各 HTML ページは、フォーム、テキスト、画像、アニメーション、リンクなどの HTML 要素で構成されています。これらの要素は、タグと、各タグが開始と終了を持つ他のいくつかのタグで表されます。全体的なレイアウト表現のために、JavaScript やスタイル シート (CSS) などのスクリプト言語で記述されたアプリケーションを埋め込むこともできます。

## 簡単な歴史 ##

HTML 仕様は、その開始と最初の公開以来、1996 年から World Wide Web Consortium (W3C) によって維持されてきました。2000 年には、国際標準 (ISO/IEC 15445:2000) にもなりました。 1999 年、HTML 4.01 が公開されました。 2004 年、Web Hypertext Application Technology Working Group (WHATWG) は、2008 年に W3C との共同成果物となった HTML5 バージョンの作業を開始しました。2014 年 10 月 28 日に完成し、標準化されました。

## HTML ファイル形式の構造 ##

HTML 4 ドキュメントは、次の 3 つの部分で構成されています。

1. HTML バージョン情報を含む行
1. 宣言的なヘッダー セクション
1. ドキュメントの実際のコンテンツを含む本文。本文は、フレーム内に本文を含めるために、BODY 要素または FRAMESET 要素によって実装できます。

各セクションの先頭または後に、空白、改行、タブ、およびコメントを付けることができます。簡単な HTML ドキュメントの例を以下に示します。

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

＃＃＃ バージョン情報 ＃＃＃

コードの最初の行、\<!DOCTYPE html> 、doctype 宣言と呼ばれ、ページがどのバージョンの HTML で記述されているかをブラウザに伝えます。HTML のバージョンに応じて、ドキュメントに使用されているドキュメント タイプ定義 (DTD) を指定するさまざまな doctype 宣言があります。各 DTD は、サポートする要素が他と異なり、次のように異なります。

* HTML 4.01 Strict - [非推奨](https://www.w3.org/TR/html401/conform.html#deprecated) になっていないか、フレームセット ドキュメントに表示されないすべての要素と属性を含む
* HTML 4.01 Transitional - 厳密な DTD のすべてに加えて、非推奨の要素と属性 (そのほとんどは視覚的な表示に関するもの) を含みます。
* HTML 4.01 フレームセット - 移行用 DTD のすべてとフレームも含まれます

**HTML5** の場合、バージョン情報は次のとおりです。

```
<!DOCTYPE html>
```

### HTML ヘッダー情報 ###

HTML ドキュメントのヘッダーには、ブラウザーによってレンダリングされない多数の HTML 要素を含めることができます。このような要素は、ページに関する情報を記述するメタデータであるか、CSS スタイルシートや JavaScript ファイルなどの外部リソースから情報を取得するために使用されるセクションを含みます。ページのヘッダーは head タグで表されます。

ページ タイトルを設定するには、 **title** 要素だけが<head>タグ。同じことが、ページのタイトルを識別するために検索エンジンによって使用されます。

### HTML 本文情報 ###

これは、ブラウザによってレンダリングされるファイルのすべてのコンテンツを含むファイルのメイン セクションです。 Html 本文には、タグの形でさまざまなビルディング ブロックを参照できるマークアップを含めることができます。テキスト、画像、色、グラフィックスなど、さまざまな種類の情報を含めることができます。さらに、オーディオおよびビデオ要素を HTML 本文に埋め込んで、ブラウザでレンダリングすることもできます。視覚表現用の最新のスタイル シート アプリケーションが存在する場合、背景色、リンクの色、テキストの色などの BODY のプレゼンテーション属性は廃止されました。したがって、以下に示すように、スタイルシートを使用して同じ効果を実現できます。

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

インライン スタイル シートは簡単に埋め込むことができ、視覚効果への迅速な適用のために、外部スタイル シートを使用すると、一度展開して多くの場所にアクセスすることがより便利になります。

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML 要素 ###

前述のように、HTML 本文内のコンテンツは、Html 要素とも呼ばれるタグで表されます。各タグには、次のように記述される属性の形式で追加情報を含めることができます。<tag attribute1#"value1" attribute2#"value2"> 、ただし、すべてのタグに属性を含める必要はありません。属性が言及されていない場合、それぞれの場合にデフォルト値が使用されます。以下は、要素の例の一部です。

#### ヘッダー ####

```
<head>
  <title>The Title</title>
</head>
```

#### 見出し ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### 段落 ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## 参照 ##

* [HTML 文書のグローバル構造](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

