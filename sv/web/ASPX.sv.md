{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","aspx-fil", "aspx-filformat", "aspx-filtyp", "fil", "typ", "vad är en aspx-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX-filformat",
  "description" :"Din filformatsguide för att lära dig vad som är en ASPX-fil och API:er som kan skapa och öppna ASPX-filer.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en ASPX fil?

En fil med filtillägget .aspx är en webbsida som genereras med hjälp av Microsoft ASP.NET-ramverket som körs på webbservrar. ASPX står för Active Server Pages Extended och dessa sidor visas i webbläsaren i användaränden när URL:en nås. Det är en efterföljare till [ASP](/sv/web/asp/)-tekniken som också genereras vid serveränden men som inte använder .NET-ramverket. ASP.NET-sidor kan innehålla skript [C#](/sv/programming/cs/) eller [VB.NET](/sv/programming/vb/) som översätts till HTML av webbservern för presentation för användare i webbläsare. ASPX-sidor kallas även .NET Web Forms. Dessa kan öppnas och skapas med applikationer som Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ och vilken textredigerare som helst.

## ASPX filformat

ASP.NET webbformulär är baserade på den händelsedrivna modellen för interaktioner med webbapplikationen. Webbläsaren, som är en slutanvändare, skickar ett webbformulär till servern och servern returnerar en fullständig uppmärkningssida eller HTML-sida som svar. ASP.NET komponentmodell erbjuder objektmodell för ASPX-sidor. Denna modell beskriver:

* Motsvarigheter på serversidan av nästan alla HTML-element eller taggar, som \<form> och \<input> .
* Serverkontroller, som hjälper till att utveckla komplexa användargränssnitt. Till exempel kontrollen Kalender eller Gridview-kontrollen.

ASPX-filer använder ASP.NET **Code Behind-modellen** för att bygga dessa sidor.

### In-Line-kod

Exempelkod som är inbäddad i ASPX-sidan och tillhandahåller all funktionalitet för användarimplementeringen. Följande [C#](/sv/programming/cs/)-kod representerar ett exempel på ASP.NET-sida som innehåller in-line-kod:

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

### Kod-bakom

Kod kan skrivas och lagras i separata klassfiler för ren separation av HTML från presentationslogik. Detta gör presentationslagret oberoende av den körbara koden. Följande är koden bakom för presentation för användaren.

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

C#-implementeringen av själva logiken för presentationslagret är som följer.

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

## Referenser

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

