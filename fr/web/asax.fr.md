{
  "date" : "2019-10-11",
  "keywords" :[ "asax","fichier asax", "format de fichier asax", "type de fichier asax", "fichier", "type", "qu'est-ce qu'un fichier asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - Fichier d'application du serveur ASP.NET",
  "description" :"Apprenez à savoir ce qu'est un fichier ASAX et les API qui peuvent créer et ouvrir des fichiers ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Qu'est-ce qu'un fichier ASAX ?

Un fichier avec l'extension .asax est un fichier utilisé par les applications ASP.NET qui réside côté serveur. Il contient du code pour répondre aux événements de niveau application et de niveau session déclenchés par ASP.NET ou par des modules HTTP. Cela inclut également la gestion de certains événements lors du lancement ou de la fermeture de l'application. Les fichiers ASAX sont facultatifs et un seul fichier ASAX est ajouté aux applications Web pour gérer les événements et les erreurs au niveau de l'application au niveau global. Contrairement aux pages ASPX, les fichiers ASAX ne contiennent aucun code pour implémenter les fonctionnalités de l'application.

## Format de fichier ASAX

Les fichiers ASAX sont écrits au format texte brut et sont lisibles par l'homme. Le fichier ASAX le plus couramment utilisé est Global.asax qui réside dans le répertoire racine d'une application ASP.NET. Les serveurs Web sont configurés pour rejeter tout appel entrant vers ce fichier afin d'interdire aux utilisateurs de télécharger ou de visualiser le code de ce fichier.

### Global.ASAX - Un exemple de format de fichier ASAX

Un seul fichier ASAX se compose de plusieurs sections écrites pour gérer les événements au niveau de l'application. Ce sont les suivants.

* **Directives d'application** - Les directives d'application sont des balises utilisées pour définir des paramètres facultatifs spécifiques à l'application à utiliser par l'analyseur ASP.NET lors du traitement du fichier Global.asax. Ces directives se trouvent au début du fichier Global.asax et sont définies comme suit.

```
<%@ directive attribut=valeur [attribut=valeur … ]%>
```
* **Blocs de déclaration de code** - Les blocs de déclaration de code sont utilisés pour définir des sections de code serveur qui sont incorporées dans les fichiers d'application ASP.NET dans le \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Blocs de rendu de code** - Ceux-ci définissent le code en ligne ou les expressions qui s'exécutent lorsque la page est rendue. Les deux styles de blocs de rendu de code incluent le code en ligne et les expressions en ligne. Le premier est utilisé pour définir des lignes ou des blocs de code autonomes, tandis que le latéral est utilisé comme raccourci pour appeler la méthode Write.

## Références

* [Présentation des gestionnaires HTTP et des modules HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax Syntax](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

