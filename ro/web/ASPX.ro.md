{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","fișier aspx", "format fișier aspx", "tip fișier aspx", "fișier", "tip", "ce este un fișier aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ASPX",
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier ASPX și API-urile care pot crea și deschide fișiere ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier ASPX?

Un fișier cu extensia .aspx este o pagină web generată folosind framework-ul Microsoft ASP.NET care rulează pe servere web. ASPX înseamnă Active Server Pages Extended și aceste pagini sunt afișate în browser web la sfârșitul utilizatorului atunci când este accesată adresa URL. Este succesorul tehnologiei [ASP](/ro/web/asp/), care sunt, de asemenea, generate la sfârșitul serverului, dar nu utilizează .NET framework. Paginile ASP.NET pot conține scripturi [C#](/ro/programming/cs/) sau [VB.NET](/ro/programming/vb/) care sunt traduse în HTML de către serverul web pentru prezentare utilizatorului în browserul web. Paginile ASPX se mai numesc și formulare web .NET. Acestea pot fi deschise și create cu aplicații precum Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ și orice editor de text.

## Format de fișier ASPX

Formularele web ASP.NET se bazează pe modelul bazat pe evenimente pentru interacțiunile cu aplicația web. Browserul, fiind un utilizator final, trimite un formular web către server, iar serverul returnează o pagină de markup completă sau o pagină HTML ca răspuns. Modelul de componentă ASP.NET oferă model obiect pentru paginile ASPX. Acest model descrie:

* Omoloage pe partea serverului a aproape toate elementele sau etichetele HTML, cum ar fi \<form> și \<input> .
* Controale server, care ajută la dezvoltarea unei interfețe complexe cu utilizatorul. De exemplu, controlul Calendar sau controlul Gridview.

Fișierele ASPX utilizează modelul ASP.NET **Code Behind** pentru construirea acestor pagini.

### Cod în linie

Exemplu de cod care este încorporat în pagina ASPX și oferă toate funcționalitățile pentru implementarea utilizatorului. Următorul cod [C#](/ro/programming/cs/) reprezintă un exemplu de pagină ASP.NET care include codul în linie:

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

### Codul din spate

Codul poate fi scris și stocat în fișiere de clasă separate pentru o separare clară a HTML de logica prezentării. Acest lucru face ca stratul de prezentare să fie independent de codul executabil. Următorul este codul din spatele pentru prezentare către utilizator.

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

Implementarea C# a logicii actuale pentru stratul de prezentare este după cum urmează.

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

## Referințe

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

