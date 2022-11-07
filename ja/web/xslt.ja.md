{
  "date" : "2021-01-20",
  "keywords" :["xslt", "ファイル", "拡張子", "ファイル形式", "ファイル拡張子", "拡張可能なスタイルシート言語"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLTファイル形式",
  "description":"XSLT ファイル形式と,XSLT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## XSLT ファイルとは?

拡張子が .xslt のファイルは、XSL 命令を使用して XML ファイルを変換およびスタイル設定するために使用される Extensible Stylesheet Language Transformation ファイルです。この形式は、XML ドキュメントをテキスト ドキュメントや .html Web ページなどの標準出力形式に変換するために使用されます。この変換により、既存の XML ドキュメントのコンテンツに基づいて新しいドキュメントが作成されます。 XSLT により、理論的には任意の計算が可能になります。

## XSLT ファイル形式

XLST ファイル形式には、任意のテキスト エディターで表示できるプレーン テキスト形式の変換命令が含まれています。言語には 3 つの改訂がありました。

* `XSLT 1.0` - XSLT 1.0 は、1999 年 11 月に W3C 勧告として公開されました。
* `XSLT 2.0` - 正規表現を使用した文字列操作、日付、時刻、期間を操作するための関数と演算子、複数の出力ドキュメント、グループ化、より豊富な型システムと強力な型チェックなどの変更が含まれています。
* `XSLT 3.0` - 2017 年 6 月 8 日に W3C 勧告の一部となりました。主な新機能には、ストリーミング変換、大きなスタイルシートのモジュール性を改善するパッケージ、xsl:try 命令などによる動的エラーの処理の改善が含まれます。マップと配列のサポートにより、XSLT で XML だけでなく JSON も処理できるようになります。

### XSLT の例

次の例は、[w3schools](https://www.w3schools.com/xml/xsl_intro.asp) からの抜粋です。
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## 参照 ##

* [XSLT - ウィキペディアによる](https://en.wikipedia.org/wiki/XSLT)
* [XSLT要素](https://en.wikipedia.org/wiki/XSLT_elements)

