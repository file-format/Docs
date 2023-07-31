{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "soubor aspx", "formát souboru aspx", "typ souboru aspx", "soubor", "typ", "co je soubor aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ASPX",
  "description" :"Váš průvodce formátem souboru, kde se dozvíte, co je soubor ASPX a rozhraní API, která mohou vytvářet a otevírat soubory ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor ASPX?

Soubor s příponou .aspx je webová stránka vygenerovaná pomocí rozhraní Microsoft ASP.NET běžící na webových serverech. ASPX je zkratka pro Active Server Pages Extended a tyto stránky jsou zobrazeny ve webovém prohlížeči na straně uživatele, když je přístup k URL. Je nástupcem technologie [ASP](/cs/web/asp/), která se také generuje na konci serveru, ale nepoužívá .NET framework. Stránky ASP.NET mohou obsahovat skripty [C#](/cs/programming/cs/) nebo [VB.NET](/cs/programming/vb/), které jsou webovým serverem přeloženy do HTML pro prezentaci uživateli ve webovém prohlížeči. Stránky ASPX se také nazývají webové formuláře .NET. Ty lze otevřít a vytvořit pomocí aplikací, jako je Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ a libovolný textový editor.

## Formát souboru ASPX

Webové formuláře ASP.NET jsou založeny na modelu řízeném událostmi pro interakce s webovou aplikací. Prohlížeč jako koncový uživatel odešle na server webový formulář a server jako odpověď vrátí úplnou značkovací stránku nebo stránku HTML. Komponentní model ASP.NET nabízí objektový model pro stránky ASPX. Tento model popisuje:

* Protějšky téměř všech prvků HTML nebo značek na straně serveru, jako je \<form> a \<input> .
* Ovládací prvky serveru, které pomáhají při vývoji komplexního uživatelského rozhraní. Například ovládací prvek Kalendář nebo ovládací prvek Gridview.

Soubory ASPX používají pro konstrukci těchto stránek model ASP.NET **Code Behind**.

### In-line kód

Ukázkový kód, který je vložen do stránky ASPX a poskytuje všechny funkce pro uživatelskou implementaci. Následující kód [C#](/cs/programming/cs/) představuje ukázkovou stránku ASP.NET, která obsahuje vložený kód:

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

### Kód-za

Kód lze zapsat a uložit do samostatných souborů třídy pro čisté oddělení HTML od prezentační logiky. Díky tomu je prezentační vrstva nezávislá na spustitelném kódu. Následuje kód pro prezentaci uživateli.

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

Implementace C# skutečné logiky pro prezentační vrstvu je následující.

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

## Reference

* [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

