{
  "date" : "2019-10-11",
  "keywords" :["xml","ファイル","拡張子","ファイル形式","ファイル拡張子","拡張マークアップ言語"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XMLファイル形式",
  "description":"XML ファイル形式と,XML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## XML ファイルとは?

XML は Extensible Markup Language の略で、**[HTML](/web/html/)** に似ていますが、オブジェクトを定義するためのタグの使用が異なります。 XML ファイル形式の作成の背後にある全体的な考え方は、ソフトウェアやハードウェア ツールに依存せずにデータを保存および転送することでした。その人気は、人間と機械の両方で読み取り可能であるためです。これにより、World Wide Web (WWW) などのネットワーク上で保存および共有されるオブジェクトの形式で、共通のデータ プロトコルを作成できます。 XML の「X」は拡張可能を意味します。これは、ユーザーの要件に応じて、言語を任意の数のシンボルに拡張できることを意味します。これらの機能のために、Microsoft Open XML、LibreOffice OpenDocument、**[XHTML](/web/xhtml/)** および **[SVG](/page-description-language/svg/)** などの多くの標準ファイル形式がそれを利用しています。.

## XML ファイル形式

XML ファイル形式は、HTML および XML ドキュメント用のプログラミング API である XML Document Object Model (DOM) に基づいています。 XML DOM は、XML ドキュメント要素にアクセスして操作するための標準メソッドを定義します。 DOM ツリーを介してすべての要素にアクセスするために使用できる XML ドキュメントのツリー構造ビューを作成します。既存の要素を変更/削除したり、XML ツリーで新しい要素を作成したりできます。 XML ドキュメントの各要素はノードと呼ばれます。 XML DOM は、次の図に示すとおりです。

{{< figure src="../XML DOM.png" alt="XMLDOM" >}}

### XML の普遍的なアプローチ

XML の力により、データ転送とプラットフォームの変更が簡素化されるため、XML はネットワークを介したデータ通信の汎用言語になります。また、これにより、データをプレーンテキスト形式で保存することにより、互換性のないシステム間でのデータ交換が可能になります。 HTML は Web 上のデータ表現用であり、XML はデータ交換用です。 XML 内で使用されるマークアップ タグのペアは、読み取りアプリケーションによって利用される構造の主要な要素を定義します。

## XML の例

以下は、各レコードにアーティスト、国、会社、価格、製造年などの CD に関する情報が含まれている CD カタログの簡単な例です。

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## 参考文献

* [XML - ウィキペディアによる](https://en.wikipedia.org/wiki/XML)

