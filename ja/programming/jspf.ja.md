{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSPフラグメントファイル形式",
  "description":"JSPF ファイル形式と,JSPF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## .JSPF ファイルとは?
拡張子が .jspf のファイルは JSP フラグメントと呼ばれます。別の JSP ファイルに含まれる静的ファイル。 JSPF ファイルは単独ではコンパイルされませんが、ファイルが含まれているページと一緒にコンパイルされます。その構文は、Java Server Pages (JSP) コードに似ています。これには、JSP のフラグメントのみが含まれています。 JSP ドキュメント全体が含まれているわけではありません。

## JSPF ファイル形式
「JSP フラグメント」という用語は JSP 2.0 仕様でオーバーロードされているため、代わりに「JSP セグメント」という用語が使用されます。 JSP フラグメントは .jsp または .jspf 拡張子を使用でき、**/WEB-INF/jspf** に配置するか、残りの静的ファイルと一緒に配置する必要があります。完全なページではない JSP フラグメントは、.jspf 拡張子を使用する必要があり、**/WEB-INF/jspf** に配置する必要があります。

### JSP または JSP フラグメント ファイルの構成
JSP ファイルには、次のセクションが記載されている順序で含まれています。

1. 冒頭のコメント
2. JSP ページ ディレクティブ
3. オプションのタグ ライブラリ ディレクティブ
4. オプションの JSP 宣言
5. HTML および JSP コード

JSP または JSPF ファイルはどちらも、**Opening Comment** と呼ばれるサーバー側スタイルのコメントで始まります。

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
このコメントは、JSP ページのレンダリング中に削除されるため、サーバー側でのみ表示できます。

## JSP フラグメント ファイルを使用する場合
JSP ページが、他の JSP ページでも再利用できる特定の複雑な構造を必要とする場合、これを処理する 1 つの方法は、複合ビュー パターン (Java ブループリントのパターン セクション) を使用して、断片に分割することです。たとえば、JSP ページのプレゼンテーション構造には、次のような論理レイアウトが含まれることがあります。

{{< figure src="../jspf.png" alt="JSPF ファイル形式" >}}

この場合、この複合 JSP ページはさまざまなモジュールに変換でき、それぞれが個別の JSP フラグメントと呼ばれます。その後、JSP フラグメントを複合 JSP ページの適切な場所に配置できます。したがって、静的インクルード ディレクティブを使用して、それ自体では呼び出されないページをインクルードする場合は、JSPF ファイルが使用されます。.jspf 拡張子を持つファイルは、Web アプリケーション アーカイブの /WEB-INF/jspf/ ディレクトリに配置する必要があります (戦争）。

## JSPF の例
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## 参考文献

* [JavaServer Pages のコード規則](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

