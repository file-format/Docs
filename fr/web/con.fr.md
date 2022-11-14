{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier CON - Format de fichier source d'application de concept",
  "description" :"Découvrez ce qu'est un fichier CON et les API qui peuvent créer et ouvrir des fichiers CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Qu'est-ce qu'un fichier CON ?

Un fichier CON est un fichier de code source pour une application développée pour **Concept Application Server**. Il est utilisé pour écrire des applications d'échange de données entre le serveur et l'utilisateur. Les fichiers CON hébergés sur le serveur sont accessibles avec un navigateur Web à condition que Concept Client soit installé côté utilisateur. Le serveur d'applications est un serveur Web avec un langage de programmation à petite échelle qui peut avoir un moteur de base de données de sous-ensemble [SQL](/fr/database/sql/) (TinDB).

Les fichiers CON peuvent s'ouvrir/s'exécuter avec RadGs Concept Application Server.

## Format de fichier CON - Plus d'informations

Les fichiers CON sont hébergés sur le serveur et sont accessibles à l'aide d'un navigateur Web sur la machine de l'utilisateur. Concept Les [URL](/fr/web/url/) sont différentes des URL HTTP normales et commencent par **concept://**.

### Exemple d'URL de fichier CON

Un fichier CON hébergé sur Concept Application Server est accessible via un navigateur Web à l'aide d'URL telles que :

```
concept://domain.server.com/web_application/main.con.
```
## Références

* [Concept Application Server] (https://github.com/Devronium/ConceptApplicationServer)

