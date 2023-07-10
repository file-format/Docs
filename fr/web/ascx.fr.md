{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","fichier ascx", "format de fichier ascx", "type de fichier ascx", "fichier", "type", "qu'est-ce qu'un fichier ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ASCX",
  "description" :"Découvrez ce qu'est un fichier ASCX et les API qui peuvent créer et ouvrir des fichiers ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier ASCX ?

Un fichier avec l'extension .ascx est un contrôle utilisateur utilisé comme composant réutilisable dans les pages Web. Il est référencé dans n'importe quel site Web ASP en le faisant glisser de la boîte de contrôle vers la page. Les contrôles des utilisateurs ASCX sont ajoutés au projet en tant que source centrale, ce qui fait que tout changement dans le contrôle de l'utilisateur est répercuté sur l'ensemble du site Web. Contrairement aux fichiers ASMX qui définissent un mécanisme pour communiquer entre 2 objets sur Internet, les fichiers ASCX sont des contrôles utilisateur pour l'intégration dans des pages ou un site Web.

## Format de fichier ASCX

Les fichiers ASCX sont écrits au format texte brut et peuvent utiliser des fonctionnalités de code derrière comme les pages Web qui se terminent par .ascx.cs. Le code de balisage des contrôles utilisateur commence par la directive @Control, comme illustré dans l'exemple suivant.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Ce contrôle de l'utilisateur Web peut être réutilisé sur de nombreuses pages telles que le pied de page, l'en-tête ou une sorte de navigation sur le site. Les contrôles utilisateur Web ont des propriétés, des méthodes et des événements comme tout autre contrôle qui les rendent utiles pour définir leur comportement visuel.

### Exemple d'enregistrement de contrôles utilisateur dans web.config

Afin d'utiliser un seul contrôle utilisateur sur plusieurs pages, le contrôle Web peut être enregistré dans web.config. Cela permet d'utiliser le contrôle sur tout le site Web au lieu de s'inscrire sur chaque page individuellement. L'exemple de code suivant définit comment enregistrer un contrôle Web dans web.config pour qu'il s'affiche en pied de page sur l'ensemble du site Web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Références

* [ASCX contre ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [Contrôle utilisateur ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

