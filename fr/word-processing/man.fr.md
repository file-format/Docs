{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manuel Unix",
  "description":"En savoir plus sur le format de fichier FODT et les API qui peuvent créer et ouvrir des fichiers MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Qu'est-ce qu'un fichier MAN ?

Un fichier avec l'extension .man signifie une page de manuel qui est un manuel de l'utilisateur de programmation Unix sous forme de documentation logicielle. Il est utilisé par l'utilitaire `Man`, inclus dans Unix, qui est utilisé pour afficher la documentation. La documentation du logiciel contient des informations dans des sections et des pages qui peuvent être récupérées à l'aide de l'utilitaire Man à partir du terminal de commande en émettant des commandes. Étant disponible dans l'ordinateur sous forme de copie électronique de la documentation, il ne nécessite aucune copie imprimée ni connexion Internet pour y accéder.

## Format de fichier Unix Manual Man - Plus d'informations

Les pages de manuel sont stockées au format texte brut et peuvent être créées et ouvertes dans n'importe quel éditeur de texte pour être visualisées ou modifiées. Sous UNIX, les informations des pages Man sont récupérées en émettant des commandes à partir du terminal qui incluent une référence aux numéros de section et de page du manuel.

### Sections et pages

Unix man est le manuel du système où chaque argument de page de la commande fait référence au nom d'un programme, d'un utilitaire ou d'une fonction. la commande, si elle est fournie avec des informations de section, recherchera la page dans cette section spécifique. Cependant, le comportement par défaut consiste à rechercher la page dans toutes les sections et à afficher la première page, qu'elle existe ou non dans plusieurs sections.

### Numéros de section

Vous trouverez ci-dessous des informations sur les numéros de section du manuel suivis des types de pages qu'ils contiennent.

|Numéro de section|Type de pages|
---|---|
|1|Programmes exécutables ou commandes shell|
|2|Appels système (fonctions fournies par le noyau)|
|3|Appels de bibliothèque (fonctions dans les bibliothèques de programmes)|
|4|Fichiers spéciaux (généralement trouvés dans /dev)|
|5|Formats et conventions de fichiers, par exemple /etc/passwd|
|6|Jeux|
|7|Divers (y compris les packages de macros et les conventions), par exemple man(7), groff(7)|
|8|Commandes d'administration système (généralement uniquement pour root)|
|9|Routines du noyau [Non standard]|

## Exemple - Comment lire les pages MAN ?

Voici un exemple de récupération d'informations sur la commande MkDir à l'aide de la commande Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Références

* [Spécifications techniques OpenDocument - Par Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — page de manuel Linux](https://man7.org/linux/man-pages/man1/man.1.html)

