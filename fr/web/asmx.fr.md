{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","fichier asmx", "format de fichier asmx", "type de fichier asmx", "fichier", "type", "qu'est-ce qu'un fichier asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - Fichier de service Web ASP.NET",
  "description" :"Découvrez ce qu'est un fichier ASMX et les API qui peuvent créer et ouvrir des fichiers ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Qu'est-ce qu'un fichier ASMX ?

Un fichier avec les extensions .asmx est un fichier de service Web ASP.NET qui assure la communication entre deux objets sur Internet à l'aide du protocole SOAP (Simple Object Access Protocol). Il est déployé en tant que service sur le serveur Web Windows pour traiter les demandes entrantes et renvoyer la réponse. Contrairement aux fichiers [ASPX](/fr/web/aspx/) qui contiennent le code pour l'affichage visuel des pages Web ASP.NET, les fichiers ASMX s'exécutent sur le serveur en arrière-plan et effectuent différentes tâches telles que la connexion à la base de données, la récupération des données et leur retour dans un format dans lequel la demande a été faite. Ceux-ci sont utilisés spécifiquement pour les services Web XML.

## Format de fichier ASMX

Les fichiers ASMX sont au format texte brut et peuvent être ouverts ou modifiés dans des applications telles que Microsoft Visual Studio ou des éditeurs de texte. Il s'agit d'un format de fichier propriétaire de Microsoft et possède une syntaxe bien définie pour la création de services Web. Une réponse par un fichier ASMX sous forme de SOAP XML comporte les éléments suivants.

* `Envelop` - Un élément racine qui identifie le document XML en tant que message SOAP.
* `Header` - Un élément facultatif qui contient des informations spécifiques à l'application telles que les données d'authentification. Si l'élément Header est présent, il doit être le premier élément enfant de l'élément Envelope.
* `Body` - Contient le message SOAP destiné au destinataire.
* `Fault` - Un élément facultatif utilisé pour indiquer les messages d'erreur. Si l'élément Fault est présent, il doit s'agir d'un élément enfant de l'élément Body.

Les fichiers ASMX peuvent être écrits dans des langages .NET tels que [C#](/fr/programming/cs/), [Visual Basic](/fr/programming/vb/) ou JScript.

## En quoi ASMX est-il différent d'ASPX et d'ASCX ?

Les fichiers ASMX sont différents des fichiers ASPX et ASCX.

* Les fichiers ASPX, Active Server Pages, sont des fichiers de programmation générés à l'aide du framework Microsoft ASP.NET exécuté sur des serveurs Web. Ceux-ci sont rendus dans le navigateur Web du client lorsque l'utilisateur demande à accéder à une telle page.
* ASCX, Active Server User Control, définit les contrôles utilisateur qui sont utilisés pour définir des contrôles réutilisables dans les pages Web ASP.NET ou dans l'ensemble du site Web.

## Références

* [Utilisation du service ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Contrôle utilisateur ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

