{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier MAÎTRE - Format de fichier de page maître ASP.NET",
  "description" :"Découvrez le format de fichier MASTER et les API pour créer et ouvrir des fichiers MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Qu'est-ce qu'un fichier MASTER ?

Un fichier MASTER est un fichier de modèle de page Web principal créé avec ASP.NET. Il est utilisé comme point de départ pour créer plusieurs pages ayant la même mise en page et les mêmes paramètres que le fichier MASTER. Le fichier modèle MASTER comprend des paramètres pour l’en-tête, les menus de navigation, le pied de page, la police et les informations de style. L'utilisation d'un fichier MASTER permet de créer rapidement plusieurs pages Web.

Vous pouvez ouvrir un fichier MASTER à l'aide de Microsoft Visual Studio 2022 et supérieur.

## Format de fichier MASTER - Plus d'informations

Un fichier MASTER est créé et enregistré au format de fichier HTML et est similaire à tout autre fichier de page Web. Il est divisé en sections modifiables et non modifiables. Les sections modifiables sont celles qui peuvent être modifiées pour répondre aux besoins de l'utilisateur. Les sections non modifiables sont grisées lorsque le fichier MASTER est ouvert dans Microsoft Visual Studio.

Les pages maîtres se composent de deux éléments, à savoir la page maître elle-même et une ou plusieurs pages de contenu.

### La page principale

La page maître a l'extension .master et est réalisée en ASP.NET. Il a une mise en page prédéfinie comprenant du texte statique, des balises HTML et des contrôles côté serveur. Dans les pages .aspx ordinaires, la directive @ Page est utilisée. Dans le cas des fichiers .master, ceci est remplacé par la directive @Master.

### Pages de contenu

Une page de contenu représente le contenu des contrôles d'espace réservé de la page maître. Ce sont des pages .aspx qui sont en fait le code-behind de la page maître. Les pages de contenu sont liées à l'aide de la directive @ Page en incluant un attribut MasterPageFile pointant vers la page maître à utiliser comme indiqué ci-dessous.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Les références

* [Présentation des pages maîtres ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

