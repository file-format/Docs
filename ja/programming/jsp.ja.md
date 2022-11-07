{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages ファイル形式",
  "description":"JSP の例と,JSP ファイルを作成して開くことができる API を使用して,JSP ファイル形式について学びます。",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## .JSP オプション番号
JSP ファイルは、Java Web アプリケーション用の動的なデータ駆動型ページとして実現されます。 JSP は Java Server Pages を意味します。式言語など、サーブレットよりも多くの機能を使用できるため、サーブレットの拡張として実現できます。 JSP とサーブレットは、古い Java Web アプリケーションで一緒に同じ仕事をします。プログラミングの観点から見ると、両者の最も明確な違いは、サーブレットでは Java プログラムを作成し、そのコードに静的マークアップ (HTML など) を埋め込むのに対し、JSP はクライアント側のスクリプトまたはマークアップで開始し、次に JSP タグを埋め込んで、ページを Java バックエンドに接続します。

## JSP ファイル形式
**jsp ファイル拡張子** で保存されたファイルには、次のセクションが記載されている順序で含まれています。

1.オープニングコメント
2. JSP ページ ディレクティブ
3. オプションのタグ ライブラリ ディレクティブ
4. オプションの JSP 宣言
5. HTML および JSP コード

### 冒頭のコメント
JSP ファイルまたはフラグメント ファイルは、サーバー サイド スタイルのコメントで始まります。

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
上記のコメントは、ブラウザでのページのレンダリング中に削除されるため、サーバー側でのみ表示されます。コメントには、作成者に関する情報、日付、リビジョンの著作権表示、開発者向けの JSP ページに関する識別子と説明が含まれる場合があります。文字 " @(#)" の組み合わせは、特定のプログラムによって、識別子の開始を示すものとして認識されます。

### JSP ページ ディレクティブ
JSP ページ ディレクティブは、変換時に JSPF ページに関連付けられた属性を定義します。 JSP 仕様では、1 ページに記述できる JSP ページ ディレクティブの数に制限はありません。次の例を参照してください。

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
ページ ディレクティブが JSP ページの通常の幅を超える場合、ディレクティブはいくつかの行に分割されます。

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### オプションのタグ ライブラリ ディレクティブ
JSP ページでは、タグ ライブラリ ディレクティブがカスタム タグ ライブラリを宣言します。短いディレクティブは 1 行で宣言できます。複数のタグ ライブラリ ディレクティブが、JSP ページの本文内の同じ場所にまとめてスタックされます。

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### オプションの JSP 宣言
  


JSPF ファイルで宣言されたメソッドと変数は、JSP 宣言に存在する必要があります。これらのメソッドと変数は、Java プログラミング言語の宣言と似ているため、関連するコード規則に従う必要があります。宣言は通常、単一の < %! で記述します。 ... %> JSP 宣言ブロック。JSP ページ本体の 1 つの領域内で宣言を集中化します。次の例を見てください。

#### 異なる宣言ブロック:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### 優先宣言ブロック:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML と JSP コード
JSP ページのこのセクションには、JSP ページの HTML 本体と、JSP 式、スクリプトレット、JavaBeans 命令などの JSPF コードが含まれます。

## JSP ページのライフサイクル

フェーズ単位の JSP ページ フローは次のとおりです。

- JSPページの翻訳
- JSP ページのコンパイル
- クラスローディング (クラスローダがクラスファイルをロード)
- インスタンス化 (生成されたサーブレットのオブジェクトが作成されます)。
- 初期化 (コンテナが jspInit() メソッドを呼び出します)。
- リクエスト処理 (コンテナが _jspService() メソッドを呼び出します)。
- 破棄します (コンテナが jspDestroy() メソッドを呼び出します)。

{{< figure src="../jsp.jpg" alt="JSP ファイル形式" >}}

## JSP の例

多くの JSP チュートリアルがインターネット上で入手できるため、JSP テクノロジーについて学ぶことは今日では非常に簡単です。次の JSP の例は、データベース内の適切なレコードを更新することによって注文を処理するためのものです。
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## 参考文献

* [JavaServer Pages のコード規約](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP チュートリアル](https://www.javatpoint.com/jsp-tutorial)

