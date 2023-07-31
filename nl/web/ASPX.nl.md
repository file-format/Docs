{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","aspx-bestand", "aspx-bestandsformaat", "aspx-bestandstype", "bestand", "type", "wat is een aspx-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX-bestandsindeling",
  "description" :"Uw gids voor bestandsindelingen om te leren wat een ASPX-bestand is en API's die ASPX-bestanden kunnen maken en openen.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een ASPX-bestand?

Een bestand met de extensie .aspx is een webpagina die is gegenereerd met behulp van het Microsoft ASP.NET-framework dat op webservers wordt uitgevoerd. ASPX staat voor Active Server Pages Extended en deze pagina's worden weergegeven in de webbrowser aan het einde van de gebruiker wanneer de URL wordt geopend. Het is de opvolger van [ASP](/nl/web/asp/)-technologie die ook aan de serverzijde wordt gegenereerd, maar geen .NET-framework gebruikt. ASP.NET-pagina's kunnen [C#](/nl/programming/cs/)- of [VB.NET](/nl/programming/vb/)-scripts bevatten die door de webserver naar HTML worden vertaald voor presentatie aan de gebruiker in de webbrowser. ASPX-pagina's worden ook wel .NET-webformulieren genoemd. Deze kunnen worden geopend en gemaakt met toepassingen zoals Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ en elke teksteditor.

## ASPX-bestandsindeling

ASP.NET-webformulieren zijn gebaseerd op het gebeurtenisgestuurde model voor interacties met de webtoepassing. De browser, die een eindgebruiker is, verzendt een webformulier naar de server en de server retourneert als reactie een volledige opmaakpagina of HTML-pagina. ASP.NET-componentmodel biedt objectmodel voor ASPX-pagina's. Dit model beschrijft:

* Server-side tegenhangers van bijna alle HTML-elementen of tags, zoals \<form> en \<input> .
* Servercontroles, die helpen bij het ontwikkelen van een complexe gebruikersinterface. Bijvoorbeeld het besturingselement Agenda of het besturingselement Gridview.

ASPX-bestanden gebruiken het ASP.NET **Code Behind-model** voor de constructie van deze pagina's.

### In-line code

Voorbeeldcode die inline is ingesloten in de ASPX-pagina en alle functionaliteit biedt voor de gebruikersimplementatie. De volgende [C#](/nl/programming/cs/)-code vertegenwoordigt een voorbeeld-ASP.NET-pagina die in-line code bevat:

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

### Code achter

Code kan worden geschreven en opgeslagen in afzonderlijke klassenbestanden voor een zuivere scheiding van HTML en presentatielogica. Dit maakt de presentatielaag onafhankelijk van de uitvoerbare code. Hieronder volgt de code-behind voor presentatie aan de gebruiker.

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

De C#-implementatie van de eigenlijke logica voor de presentatielaag is als volgt.

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

## Referenties

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

