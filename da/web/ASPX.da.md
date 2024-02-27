{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"aspx fil",
"aspx filformat",
"aspx filtype",
"fil",
"type",
"hvad er en aspx-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASPX filformat",
  "description": "Din filformatguide for at lære, hvad en ASPX-fil og API'er er, der kan oprette og åbne ASPX-filer.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-daX"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en ASPX fil?

En fil med filtypenavnet .aspx er en webside, der er genereret ved hjælp af Microsoft ASP.NET framework, der kører på webservere. ASPX står for Active Server Pages Extended, og disse sider vises i webbrowseren i brugerenden, når URL'en tilgås. Det er efterfølgeren til [ASP](/web/asp/)-teknologien, som også genereres ved serverenden, men som ikke bruger .NET framework. ASP.NET-sider kan indeholde [C#](/programming/cs/)- eller [VB.NET](/programming/vb/)-scripts, der er oversat til HTML af webserveren til præsentation for brugeren i webbrowseren. ASPX-sider kaldes også .NET Web Forms. Disse kan åbnes og oprettes med programmer som Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ og enhver teksteditor.

## ASPX filformat

ASP.NET webformularer er baseret på den hændelsesdrevne model for interaktioner med webapplikationen. Browseren, der er slutbruger, sender en webformular til serveren, og serveren returnerer en fuld opmærkningsside eller HTML-side som svar. ASP.NET komponentmodel tilbyder objektmodel til ASPX-sider. Denne model beskriver:

 * Serverside-modstykker til næsten alle HTML-elementer eller tags, såsom \<form> og \<input> .
 * Serverkontroller, som hjælper med at udvikle kompleks brugergrænseflade. For eksempel kontrolelementet Kalender eller Gridview-kontrolelementet.

ASPX-filer bruger ASP.NET **Code Behind-modellen** til konstruktion af disse sider.

### In-line kode

Eksempelkode, der er indlejret inline på ASPX-siden og giver al funktionaliteten til brugerimplementeringen. Følgende [C#](/programming/cs/)-kode repræsenterer en eksempel ASP.NET-side, der indeholder in-line kode:

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

### Kode-bag

Kode kan skrives og gemmes i separate klassefiler for ren adskillelse af HTML fra præsentationslogik. Dette gør præsentationslaget uafhængigt af den eksekverbare kode. Følgende er koden bag til præsentation for brugeren.

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

C#-implementeringen af den faktiske logik for præsentationslaget er som følger.

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

## Referencer

 * [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

