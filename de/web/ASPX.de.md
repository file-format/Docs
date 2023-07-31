{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "aspx-Datei", "aspx-Dateiformat", "aspx-Dateityp", "Datei", "Typ", "was ist eine aspx-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX-Dateiformat",
  "description" :"Ihr Dateiformat-Leitfaden, um zu erfahren, was eine ASPX-Datei und APIs sind, die ASPX-Dateien erstellen und öffnen können.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine ASPX-Datei?

Eine Datei mit der Erweiterung .aspx ist eine Webseite, die mit dem Microsoft ASP.NET-Framework erstellt wurde, das auf Webservern ausgeführt wird. ASPX steht für Active Server Pages Extended und diese Seiten werden im Webbrowser auf Benutzerseite angezeigt, wenn auf die URL zugegriffen wird. Es ist der Nachfolger der [ASP](/de/web/asp/)-Technologie, die ebenfalls serverseitig generiert wird, aber kein .NET-Framework verwendet. ASP.NET-Seiten können [C#](/de/programming/cs/)- oder [VB.NET](/de/programming/vb/)-Skripts enthalten, die vom Webserver in HTML übersetzt werden, um sie dem Benutzer im Webbrowser anzuzeigen. ASPX-Seiten werden auch als .NET-Webformulare bezeichnet. Diese können mit Anwendungen wie Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ und jedem Texteditor geöffnet und erstellt werden.

## ASPX-Dateiformat

ASP.NET-Webformulare basieren auf dem ereignisgesteuerten Modell für Interaktionen mit der Webanwendung. Der Browser, der ein Endbenutzer ist, übermittelt ein Webformular an den Server, und der Server gibt als Antwort eine vollständige Markup-Seite oder HTML-Seite zurück. Das ASP.NET-Komponentenmodell bietet ein Objektmodell für ASPX-Seiten. Dieses Modell beschreibt:

* Serverseitige Entsprechungen fast aller HTML-Elemente oder -Tags, wie z. B. \<form> und \<input> .
* Serversteuerelemente, die bei der Entwicklung komplexer Benutzeroberflächen helfen. Beispielsweise das Calendar-Steuerelement oder das Gridview-Steuerelement.

ASPX-Dateien verwenden das **Code Behind-Modell** von ASP.NET zum Erstellen dieser Seiten.

### Inline-Code

Beispielcode, der Inline in die ASPX-Seite eingebettet ist und alle Funktionen für die Benutzerimplementierung bereitstellt. Der folgende [C#](/de/programming/cs/)-Code stellt eine ASP.NET-Beispielseite dar, die Inline-Code enthält:

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

### CodeBehind

Code kann geschrieben und in separaten Klassendateien gespeichert werden, um HTML sauber von der Präsentationslogik zu trennen. Dadurch wird die Präsentationsschicht unabhängig vom ausführbaren Code. Es folgt der Code-Behind zur Präsentation für den Benutzer.

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

Die C#-Implementierung der eigentlichen Logik für die Präsentationsschicht sieht wie folgt aus.

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

## Verweise

* [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

