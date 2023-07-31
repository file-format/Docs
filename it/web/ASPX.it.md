{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","file aspx", "formato di file aspx", "tipo di file aspx", "file", "tipo", "che cos'è un file aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file ASPX",
  "description" :"La tua guida al formato di file per sapere cos'è un file ASPX e le API che possono creare e aprire file ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file ASPX?

Un file con estensione .aspx è una pagina Web generata utilizzando il framework Microsoft ASP.NET in esecuzione su server Web. ASPX sta per Active Server Pages Extended e queste pagine vengono visualizzate nel browser Web all'estremità dell'utente quando si accede all'URL. È il successore della tecnologia [ASP](/it/web/asp/) anch'essa generata sul lato server ma non utilizza il framework .NET. Le pagine ASP.NET possono contenere script [C#](/it/programming/cs/) o [VB.NET](/it/programming/vb/) che vengono tradotti in HTML dal server Web per la presentazione all'utente nel browser Web. Le pagine ASPX sono anche chiamate Web Form .NET. Questi possono essere aperti e creati con applicazioni come Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ e qualsiasi editor di testo.

## Formato file ASPX

I moduli Web ASP.NET si basano sul modello basato su eventi per le interazioni con l'applicazione Web. Il browser, essendo un utente finale, invia un modulo Web al server e il server restituisce in risposta una pagina di markup completa o una pagina HTML. Il modello del componente ASP.NET offre un modello a oggetti per le pagine ASPX. Questo modello descrive:

* Controparti lato server di quasi tutti gli elementi o tag HTML, come \<form> e \<input> .
* Controlli del server, che aiutano nello sviluppo di interfacce utente complesse. Ad esempio, il controllo Calendar o il controllo Gridview.

I file ASPX utilizzano il **modello Code Behind** di ASP.NET per la costruzione di queste pagine.

### Codice in linea

Codice di esempio incorporato nella pagina ASPX e fornisce tutte le funzionalità per l'implementazione dell'utente. Il seguente codice [C#](/it/programming/cs/) rappresenta una pagina ASP.NET di esempio che include codice in linea:

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

### Code-Behind

Il codice può essere scritto e archiviato in file di classe separati per una netta separazione dell'HTML dalla logica di presentazione. Ciò rende il livello di presentazione indipendente dal codice eseguibile. Di seguito è riportato il code-behind per la presentazione all'utente.

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

L'implementazione C# della logica effettiva per il livello di presentazione è la seguente.

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

## Riferimenti

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

