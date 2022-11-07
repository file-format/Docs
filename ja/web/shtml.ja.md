{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","shtml ファイル", "shtml ファイル形式", "shtml ファイルの種類", "ファイル", "種類", "shtml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - サーバー側インクルード HTML ファイル",
  "description":"SHTML ファイル形式と,SHTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## .SHTML ファイルとは?

拡張子が .shtml のファイルは、[HTML](/web/html/) で記述された Web ページで、サーバーの説明が含まれています。また、読み込みを高速化するために、ASP ファイルに似たサーバー側のインクルードが含まれている場合もあります。サーバー側のファイルには、サーバーのロードを通常より遅くする実行可能コードが含まれている場合もあります。 SHTML ファイルは HTML に似ていますが、単純なサーバー コマンドも使用できます。これらのサーバー コマンドは、サーバー サイド インクルード (SSI) と呼ばれる単純なコンピューター プログラミング言語で実行されます。 SHTML は、[PHP](/programming/php/) インクルードなどの他のサーバー側プログラミング言語に大きく取って代わられています。

## SHTML ファイル形式

SHTML ファイルはプレーン テキストで記述され、サーバー側で実行される [SSI コマンド](https://www.w3.org/Jigsaw/Doc/User/SSI.html) を使用します。これらのサーバー側コマンドは、データベース ドライバーを使用してデータベースに接続し、テーブルからユーザー データをフェッチするためにも使用できます。

## SHTML の例

サーバー側の命令は、ページの訪問者カウンターや Web ページのカレンダーなどのアプリケーションで使用されます。次の例では、users データベースの最初の 3 行の最初の 4 列を表示します。

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## 参考文献

* [サーバー側インクルード](https://en.wikipedia.org/wiki/Server_Side_Includes)

