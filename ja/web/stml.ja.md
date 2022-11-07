{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml ファイル", "stml ファイル形式", "stml ファイルの種類", "ファイル", "種類", "stml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML ファイル",
  "description":"STML ファイル形式と,STML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## .STML ファイルとは?

拡張子が .stml のファイルは、ユーザーが Web ブラウザーでページをロードしたときに実行されるサーバー側の命令を含む Web ページです。 STML ページには、プレーンな HTML では実現できないタスクを実行するためのサーバー サイド インクルードを含むサーバー サイド コードが含まれています。 [HTML](/web/html/) に似ていますが、STML は、サーバー サイド インクルード (SSI) とも呼ばれるサーバー上でコマンドを実行することにより、より強力な機能を提供します。 PHP などのサーバー サイド スクリプトを使用した新しいプログラミング言語の導入により、STML の使用は減少していますが、STML はすべてのサーバー サイド テクノロジでサポートされています。 STML ファイルは、任意のテキスト エディターで開いて、コマンドを更新するために編集できます。

## STML ファイル形式

STML は、人間が読めるプレーンな ASCII テキスト ファイル形式に基づいています。ただし、サーバー側で実行される [SSI コマンド](https://www.w3.org/Jigsaw/Doc/User/SSI.html) を使用して定義および実行される構文に従います。他のサーバー側スクリプト言語と同様に、STML はサーバー側コマンドを使用して、ページ ビジター カウンター、Web ページ カレンダー、データベースからのレコードの取得などのタスクを実行できます。

## STML の例

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

