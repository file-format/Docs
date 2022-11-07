{
  "date" : "2021-03-23",
  "keywords" :["NCX","EPUB ナビゲーション コントロール XML ファイル","拡張子","フォーマット","電子書籍","TOC","DAISY コンソーシアム"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPUB ナビゲーション コントロール XML ファイル (NCX) ファイル形式と,NCX ファイルを作成して開くことができる API について学びます。",
  "title" :"NCX - EPUB ナビゲーション コントロール XML ファイル",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .NCX オプション番号##

XML のナビゲーション コントロール ファイルと省略された NCX ファイルで、通常は toc.ncx という名前です。このファイルは、EPUB ファイルの階層的な目次で構成されています。 NCX の仕様は Digital Talking Book (DTB) 用に開発されたもので、このファイル形式は **DAISY コンソーシアム**によって維持されており、EPUB 仕様の一部ではありません。 NCX ファイルには、**application/x-dtbncx+xml** の MIME タイプが含まれています。

## NCX 仕様 ##

NCX ファイルには、さまざまな種類の XML タグが含まれています。 `meta name="dtb:uid"` のようなメタ タグは、ID に言及するために使用されます。 `meta name="dtb:depth"` 要素は、`navMap` タグ要素の深さに等しく設定されます。 「navPoint」要素をネストして、階層的な目次を作成できます。 「navLabel」のコンテンツは、.ncx を使用する読み取りシステムによって生成された目次に表示されるテキストです。 「navPoint」要素のコンテンツは、マニフェストにリストされているコンテンツ ドキュメントを指し、要素識別子を含めることもできます

EPUB で使用される NCX 仕様に対する特定の例外の説明。ここでは、NCX ファイルの例を表示できます。

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## 参照 ##

* [ウィキペディアからの EPUB](https://en.wikipedia.org/wiki/EPUB)
* [toc.ncx に含めるファイル](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

