{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier AXD - Format de fichier du gestionnaire Web ASP.NET",
  "description" :"Découvrez ce qu'est un fichier AXD et les API qui peuvent créer et ouvrir des fichiers AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Qu'est-ce qu'un fichier AXD ?

Un fichier AXD est un fichier de paramètres Web utilisé pour gérer et récupérer les demandes de ressources intégrées dans ASP.NET. Il comprend des instructions pour récupérer des ressources intégrées telles que des images, des fichiers JavaScript ([.JS](/fr/web/js/)) et des fichiers [.CSS](/fr/web/css/). Les fichiers AXD sont utilisés pour injecter des ressources dans les pages côté client. Cela permet aux pages client d'accéder à ces ressources sur le serveur de manière standard.

## Format de fichier AXD

Les fichiers AXD sont stockés sous forme de fichiers binaires côté serveur. Il fait référence à un fichier Web Handler dans ASP.NET qui sont des composants qui génèrent des réponses à des requêtes spécifiques adressées à un serveur Web. Les fichiers AXD effectuent un traitement personnalisé avant de générer la réponse en fonction des requêtes de page côté client. Ceux-ci sont généralement enregistrés sous forme de fichiers **WebResource.axd**.

### Qu'est-ce que le fichier WebResource.axd ?

La plupart des projets ASP.NET enregistrent les fichiers AXD sous forme de fichiers WebResource.axd qui permettent aux pages côté client de télécharger des ressources intégrées dans un assembly. Votre application peut être confrontée à des performances lentes si vous l'exécutez en mode débogage, car le gestionnaire WebResources.axd n'est pas mis en cache.

## Les références

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

