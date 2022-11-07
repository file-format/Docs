{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX ファイル - HTML 拡張ファイル形式",
  "description" :"HTX ファイルとは何か,および HTX ファイルを作成して開くことができる API を学ぶためのファイル形式ガイド。",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTX ファイルとは?

HTX ファイルは実際には、データベース クエリの結果を Web ページとして表示するためのデータ変数を含む HTML ファイルです。ほとんどの場合、Microsoft FrontPage Web 開発ソフトウェアで作成された HTX ファイルは、対応するインターネット データベース コネクタ (.IDC) ファイルと同じフォルダーに保存されます。

HTX ファイルは、Microsoft FrontPage などのアプリケーションや、メモ帳、TextEdit、Atom などの任意のテキスト エディターで開くことができます。

## HTX ファイル形式

HTX ファイルは、データベースからデータを取得し、表示用に変数に保存するためのコードを含むプレーン テキスト ファイルとして保存されます。


### HTX ファイルの例

HTX ファイルの例は次のとおりです。これは、クエリ制限を表示するためのページ ヘッダーと、ユーザーに表示するためにページに表示されるドキュメントを定義します。

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

このサンプル コードの出力は次のとおりです。

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

ご覧のとおり、HTX ファイルは、結果が返されてエンド ユーザーに表示される方法をフォーマットするテンプレートです。 HTML 形式で書かれており、いくつかの IIS 拡張機能と Indexing Service が含まれています。これらの拡張機能には、結果を処理するための変数名やその他のコードが含まれます。

## 参考文献

* [結果を .Htx ファイルにフォーマットする](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

