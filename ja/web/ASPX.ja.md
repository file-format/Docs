{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","aspx ファイル", "aspx ファイル形式", "aspx ファイルの種類", "ファイル", "種類", "aspx ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPXファイル形式",
  "description" :"ASPX ファイルとは何か,および ASPX ファイルを作成して開くことができる API を学ぶためのファイル形式ガイド。",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## .ASPX オプション番号

拡張子が .aspx のファイルは、Web サーバーで実行されている Microsoft ASP.NET フレームワークを使用して生成された Web ページです。 ASPX は Active Server Pages Extended の略で、URL にアクセスすると、これらのページがユーザー側の Web ブラウザーに表示されます。これは、同じくサーバー側で生成される [ASP](/web/asp/) テクノロジの後継ですが、.NET フレームワークを使用しません。 ASP.NET ページには、[C#](/programming/cs/) または [VB.NET](/programming/vb/) スクリプトが含まれている場合があります。これらのスクリプトは、Web サーバーによって HTML に変換され、Web ブラウザーでユーザーに表示されます。 ASPX ページは、.NET Web フォームとも呼ばれます。これらは、Microsoft Visual Studio、Adobe Dreamweaver、Notepad++、および任意のテキスト エディターなどのアプリケーションで開いて作成できます。

## ASPX ファイル形式

ASP.NET Web フォームは、Web アプリケーションとの対話のためのイベント ドリブン モデルに基づいています。エンド ユーザーであるブラウザーが Web フォームをサーバーに送信すると、サーバーは応答として完全なマークアップ ページまたは HTML ページを返します。 ASP.NET コンポーネント モデルは、ASPX ページのオブジェクト モデルを提供します。このモデルは次のことを説明します。

* ほぼすべての HTML 要素またはタグのサーバー側対応物 (\ など)<form>と \<input> .
* 複雑なユーザー インターフェイスの開発に役立つサーバー コントロール。たとえば、Calendar コントロールや Gridview コントロールです。

ASPX ファイルは、これらのページの構築に ASP.NET **コード ビハインド モデル**を使用します。

### インライン コード

ASPX ページにインラインで埋め込まれ、ユーザー実装のすべての機能を提供するサンプル コードです。次の [C#](/programming/cs/) コードは、インライン コードを含むサンプル ASP.NET ページを表しています。

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### コードビハインド

HTML をプレゼンテーション ロジックから明確に分離するために、コードを別のクラス ファイルに記述して格納することができます。これにより、プレゼンテーション層が実行可能コードから独立します。以下は、ユーザーに提示するためのコード ビハインドです。

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

プレゼンテーション層の実際のロジックの C# 実装は次のとおりです。

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## 参考文献

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

