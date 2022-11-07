{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax ファイル", "asax ファイル形式", "asax ファイルの種類", "ファイル", "種類", "asax ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET サーバー アプリケーション ファイル",
  "description" :"ASAX ファイルとは何か,および ASAX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## .ASAX ファイルとは?

拡張子が .asax のファイルは、サーバー側に常駐する ASP.NET アプリケーションで使用されるファイルです。これには、ASP.NET または HTTP モジュールによって発生したアプリケーション レベルおよびセッション レベルのイベントに応答するためのコードが含まれています。これには、アプリケーションの起動時またはシャットダウン時の特定のイベントの処理も含まれます。 ASAX ファイルはオプションであり、グローバル レベルでアプリケーション レベルのイベントとエラーを処理するために、1 つの ASAX ファイルのみが Web アプリケーションに追加されます。 ASPX ページとは異なり、ASAX ファイルには、アプリケーションの機能を実装するためのコードは含まれていません。

## ASAX ファイル形式

ASAX ファイルはプレーン テキスト ファイル形式で記述されており、人間が判読できます。最も一般的に使用される ASAX ファイルは、ASP.NET アプリケーションのルート ディレクトリにある Global.asax です。 Web サーバーは、このファイルへの着信呼び出しを拒否して、ユーザーがこのファイルのコードをダウンロードまたは表示することを禁止するように構成されています。

### Global.ASAX - ASAX ファイル形式の例

1 つの ASAX ファイルは、アプリケーション レベルのイベントを処理するために記述された複数のセクションで構成されます。これらは以下の通りです。

* **アプリケーション ディレクティブ** - アプリケーション ディレクティブは、Global.asax ファイルの処理時に ASP.NET パーサーによって使用されるオプションのアプリケーション固有の設定を定義するために使用されるタグです。これらのディレクティブは Global.asax ファイルの先頭にあり、次のように定義されています。

```
<%@ ディレクティブ 属性=値 [属性=値 … ]%>
```
* **コード宣言ブロック** - コード宣言ブロックは、\ 内の ASP.NET アプリケーション ファイルに埋め込まれたサーバー コードのセクションを定義するために使用されます。<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - ページのレンダリング時に実行されるインライン コードまたは式を定義します。コード レンダー ブロックの 2 つのスタイルには、インライン コードとインライン式が含まれます。前者はコードの自己完結型の行またはブロックを定義するために使用され、横方向は Write メソッドを呼び出すためのショートカットとして使用されます。

## 参考文献

* [HTTP ハンドラーと HTTP モジュールの概要](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax 構文](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

