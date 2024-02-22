{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier STR - Fichier objet de liste de structures dBASE - Qu'est-ce que le fichier .str et comment l'ouvrir ?",
  "description" : "Découvrez le fichier objet de liste de structures STR dBASE et comment l'ouvrir.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-fr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Qu'est-ce qu'un fichier STR ?

Le format de fichier STR est généralement associé à dBASE, un système de gestion de base de données. Dans dBASE, un fichier .str représente généralement un fichier objet de liste de structures. Ce fichier contient la structure d'une table de base de données, y compris des informations sur les champs (colonnes) et leurs propriétés.

Le fichier objet de liste de structures (.str) contient des métadonnées telles que les noms de champs, les types de données, les longueurs de champs et toute autre propriété associée à chaque champ de la table de base de données. Il est utilisé pour définir la structure de la table de base de données sans contenir d'enregistrements de données réels.

Des programmes tels que dBASE ou d'autres outils de gestion de base de données peuvent utiliser ce fichier pour comprendre la disposition de la table de base de données et effectuer des opérations telles que l'interrogation, la mise à jour ou la création de nouveaux enregistrements basés sur cette structure.

Voici un exemple simple de ce qu'un fichier STR peut contenir :

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Cet exemple décrit une table avec quatre champs : ID, Nom, Âge et DOB, ainsi que leurs types et longueurs de données respectifs.

## Comment ouvrir le fichier STR?

La principale façon d'ouvrir les fichiers .str consiste à utiliser dBASE lui-même, en particulier sur les systèmes d'exploitation Windows. dBASE est capable de lire et d'interpréter le contenu de ces fichiers, permettant aux utilisateurs de visualiser et de travailler avec la structure de la base de données.

Étant donné que les fichiers .str sont essentiellement des fichiers de texte brut contenant des informations sur la structure de la base de données, vous pouvez également les ouvrir à l'aide d'un éditeur de texte. Des exemples d'éditeurs de texte incluent Microsoft Notepad sur Windows et Apple TextEdit sur Mac. Lorsqu'il est ouvert dans un éditeur de texte, vous pourrez voir le contenu du fichier, y compris les noms de champs, les types de données et d'autres informations structurelles, dans un format lisible par l'homme.

## Les références
* [dBase](https://en.wikipedia.org/wiki/DBase)


