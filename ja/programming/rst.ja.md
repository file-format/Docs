{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST ファイル形式 - reStructuredText ファイル",
  "description":"RST ファイル形式と,RST ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## .RST ファイルとは何ですか?

RST ファイルは、主に Python プログラミング コミュニティで使用される技術ドキュメント ファイル形式です。これは、reStructuredText マークアップ言語で記述されたテキスト ファイルであり、スタイルとフォーマットをプレーン テキスト ドキュメントに適用してドキュメントを生成します。 RST ファイルは、Python プログラム コード内のコメントやその他の情報を使用して、アプリケーションの技術文書を作成します。ただし、これらには、単純な Web ページや [eBook](/ebook/) に変換できるテキストを含めることもできます。 Github Atom、GNU Emacs (クロスプラットフォーム)、Microsoft Notepad (Windows)、Apple TextEdit (Mac)、Vim (Linux) などのテキスト エディターを使用して RST ファイルを開くことができます。

## RST ファイル形式

RST ファイルには、reStructuredText マークアップ言語で記述されたコードが含まれています。これは、Python Doc-SIG (Documentation Special Interest Group) の Docutils プロジェクトの一部であり、Java 用の Javadoc に似た一連の Python 用ツールを提供します。 RST ファイル形式のパーサーは Docutils に組み込まれており、Python プログラムから情報を抽出して、プログラム ドキュメントにフォーマットすることができます。

### reStructuredText RST の例

次のように RST ファイル形式で記述されたテキストの例を見てみましょう。

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

このテキストを Docutils などの rST プロセッサに入力すると、出力は次のようになります。

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## 参照 ＃＃

* [reStructuredText - ウィキペディアによる](https://en.wikipedia.org/wiki/ReStructuredText)

