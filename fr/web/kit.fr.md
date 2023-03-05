{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier KIT et les API qui peuvent créer et ouvrir des fichiers KIT.",
  "title" :"Format de fichier KIT - Fichier CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Qu'est-ce qu'un fichier KIT ?

Un fichier avec l'extension .kit est un fichier HTML créé avec l'application de langage de programmation [CodeKit](https://codekitapp.com/). Il contient des "importations" et des "variables" en plus des fichiers [HTML](/fr/web/html/) existants, ce qui le rend idéal pour les sites statiques. CodeKit compile les fichiers KIT en HTML qui peuvent être facilement utilisés comme fichiers de site Web statiques.

## Format de fichier KIT

Les fichiers KIT sont des fichiers HTML qui incluent en outre des importations et des variables. Ceux-ci sont stockés sous forme de fichiers texte brut et peuvent être ouverts avec n'importe quel éditeur de texte ou éditeur de fichiers Web.

### Importations de fichiers KIT

Presque tous les types de fichiers peuvent être importés dans un fichier Kit. Voici la syntaxe d'importation utilisée pour importer des fichiers dans un fichier .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Lorsqu'une importation est ajoutée à un fichier KIT et enregistrée, elle est remplacée par le texte du fichier importé. Vous pouvez également utiliser @include au lieu de @import.

### Importations multiples dans un fichier KIT

Vous pouvez également importer plusieurs fichiers à la fois en utilisant une liste séparée par des virgules :

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Références

* [Qu'est-ce que Kit ?](https://codekitapp.com/help/kit/)

