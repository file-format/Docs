{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","fichier jhtml", "format de fichier jhtml", "type de fichier jhtml", "fichier", "type", "qu'est-ce qu'un fichier jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Fichier HTML Java",
  "description":"En savoir plus sur le format de fichier JHTML et les API qui peuvent créer et ouvrir des fichiers JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Qu'est-ce qu'un fichier JHTML ?

Un fichier avec l'extension .jhtml est un fichier [HTML](/fr/web/html/) avec du code [Java](/fr/programming/java/) qui est exécuté sur le serveur lorsqu'un client demande cette page dans un navigateur. Le serveur traite les requêtes, exécute les fonctions Java contenues dans la fonction et renvoie la page au navigateur du client. Les objets Java intégrés dans les pages JHTML s'exécutent sur le serveur pour gérer les demandes de pages de ce type. Les fichiers JHTML peuvent également accéder aux informations de la base de données à l'aide de la connexion JDBC (Java [Database](/fr/database/) Connectivity). Les fichiers JHTML peuvent être ouverts dans n'importe quel éditeur de texte et affichés dans des navigateurs Web tels que Google Chrome, Firefox et Safari.

## Format de fichier JHTML

JHTML est une technologie propriétaire d'ATG et peut être créé à l'aide de l'éditeur de documents Dynamo d'ATG (Art Technology Group). Les fichiers JHTML sont écrits au format de fichier texte brut à l'aide du code HTML et Java standard. Ceux-ci contiennent des balises HTML standard en plus des balises propriétaires qui référencent des objets Java. Lorsqu'une telle page est demandée par l'utilisateur, le serveur HTTP transmet la demande à un serveur d'application Java. La page JHTML est d'abord convertie en fichier .java et compilée pour générer un fichier [.class](/fr/programming/class/) qui est exécuté en tant que servlet. Cela génère un flux de données HTTP et HTML standard qui sont renvoyées au navigateur demandeur pour être affichées à l'utilisateur. Ceci est utile pour exécuter des requêtes liées à la base de données sur le serveur et renvoyer le résultat cumulé finalisé au navigateur du client.

## Références

* [La structure globale du document HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

