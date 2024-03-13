{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"aspx faylı",
"aspx fayl formatı",
"aspx fayl növü",
"fayl",
"növü",
"aspx faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASPX fayl formatı",
  "description": "ASPX faylı və ASPX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənmək üçün fayl formatı bələdçisi.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-azX"
}
},
  "lastmod": "2020-09-10"
}

## ASPX faylı nədir?

.aspx genişləndirilməsi olan fayl veb serverlərdə işləyən Microsoft ASP.NET çərçivəsi ilə yaradılan veb səhifədir. ASPX, Active Server Pages Extended mənasını verir və bu səhifələr URL-ə daxil olduqda istifadəçinin sonunda veb brauzerdə göstərilir. O, həmçinin server sonunda yaradılan, lakin .NET çərçivəsini istifadə etməyən [ASP](/web/asp/) texnologiyasının varisidir. ASP.NET səhifələrində istifadəçiyə veb brauzerdə təqdim etmək üçün veb server tərəfindən HTML-yə tərcümə edilən [C#](/programming/cs/) və ya [VB.NET](/programming/vb/) skriptlər ola bilər. ASPX səhifələrinə .NET Veb Formları da deyilir. Bunlar Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ və istənilən mətn redaktoru kimi proqramlarla açıla və yaradıla bilər.

## ASPX fayl formatı

ASP.NET veb formaları veb tətbiqi ilə qarşılıqlı əlaqə üçün hadisəyə əsaslanan modelə əsaslanır. Brauzer son istifadəçi olaraq serverə veb formasını təqdim edir və server cavab olaraq tam işarələmə səhifəsini və ya HTML səhifəsini qaytarır. ASP.NET komponent modeli ASPX səhifələri üçün obyekt modeli təklif edir. Bu model təsvir edir:

 * Demək olar ki, bütün HTML elementlərinin və ya teqlərinin server tərəfindəki analoqları, məsələn \<form> və \<input> .
 * Mürəkkəb istifadəçi interfeysini inkişaf etdirməyə kömək edən server idarəetmələri. Məsələn, Təqvim nəzarəti və ya Gridview nəzarəti.

ASPX faylları bu səhifələrin qurulması üçün ASP.NET **Code Behind model**-dən istifadə edir.

### In-Line Kod

ASPX səhifəsinə daxil edilmiş və istifadəçinin tətbiqi üçün bütün funksionallığı təmin edən nümunə kod. Aşağıdakı [C#](/programming/cs/) kodu sıra daxili kodu ehtiva edən nümunə ASP.NET səhifəsini təmsil edir:

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

### Kod-Arxada

HTML-nin təqdimat məntiqindən təmiz ayrılması üçün kod ayrı sinif fayllarında yazıla və saxlanıla bilər. Bu, təqdimat qatını icra olunan koddan müstəqil edir. Aşağıda istifadəçiyə təqdimat üçün arxa kod verilmişdir.

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

Təqdimat təbəqəsi üçün faktiki məntiqin C# tətbiqi aşağıdakı kimidir.

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

## İstinadlar

 * [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

