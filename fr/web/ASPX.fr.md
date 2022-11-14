{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "fichier aspx", "format de fichier aspx", "type de fichier aspx", "fichier", "type", "qu'est-ce qu'un fichier aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ASPX",
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier ASPX et les API qui peuvent créer et ouvrir des fichiers ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier ASPX ?

Un fichier avec l'extension .aspx est une page Web générée à l'aide du framework Microsoft ASP.NET exécuté sur des serveurs Web. ASPX signifie Active Server Pages Extended et ces pages sont affichées dans le navigateur Web à la fin de l'utilisateur lorsque l'URL est accessible. Il succède à la technologie [ASP](/fr/web/asp/) qui est également générée côté serveur mais n'utilise pas le framework .NET. Les pages ASP.NET peuvent contenir des scripts [C#](/fr/programming/cs/) ou [VB.NET](/fr/programming/vb/) qui sont traduits en HTML par le serveur Web pour être présentés à l'utilisateur dans le navigateur Web. Les pages ASPX sont également appelées formulaires Web .NET. Ceux-ci peuvent être ouverts et créés avec des applications telles que Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ et n'importe quel éditeur de texte.

## Format de fichier ASPX

Les formulaires Web ASP.NET sont basés sur le modèle événementiel pour les interactions avec l'application Web. Le navigateur, en tant qu'utilisateur final, soumet un formulaire Web au serveur et le serveur renvoie une page de balisage complète ou une page HTML en réponse. Le modèle de composant ASP.NET offre un modèle d'objet pour les pages ASPX. Ce modèle décrit :

* Homologues côté serveur de presque tous les éléments ou balises HTML, tels que \<form> et \<input> .
* Contrôles du serveur, qui aident à développer une interface utilisateur complexe. Par exemple, le contrôle Calendar ou le contrôle Gridview.

Les fichiers ASPX utilisent le modèle **Code Behind** ASP.NET pour la construction de ces pages.

### Code en ligne

Exemple de code intégré en ligne dans la page ASPX et fournissant toutes les fonctionnalités pour l'implémentation de l'utilisateur. Le code [C#](/fr/programming/cs/) suivant représente un exemple de page ASP.NET qui inclut du code en ligne :

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

### Code derrière

Le code peut être écrit et stocké dans des fichiers de classe séparés pour une séparation nette du HTML de la logique de présentation. Cela rend la couche de présentation indépendante du code exécutable. Voici le code-behind pour la présentation à l'utilisateur.

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

L'implémentation C# de la logique réelle pour la couche de présentation est la suivante.

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

## Références

* [Applications Web ASP.NET - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

