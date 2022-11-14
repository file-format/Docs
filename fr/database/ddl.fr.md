{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DDL et les API qui peuvent créer et ouvrir des fichiers DDL.",
  "title" :"Format de fichier DDL - Un fichier de langage de définition de données",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Qu'est-ce qu'un fichier DDL ?

Un fichier avec l'extension .ddl est un fichier Data Definition Language utilisé pour définir le schéma d'une base de données. Il contient des instructions/commandes pour travailler avec des structures de base de données telles que des tables, des colonnes, des enregistrements et d'autres champs. Les commandes d'un fichier DDL sont écrites en [SQL](/fr/database/sql/) et peuvent effectuer des opérations telles que créer une table dans la base de données, supprimer et mettre à jour. Un schéma de base de données appartient à sa création et toutes les opérations CRUD peuvent être effectuées dessus. Les applications populaires qui peuvent créer et ouvrir des fichiers DDL sont Windows Text Editor, Jetbrains Intellij Idea et EclipseLink.

## Commandes DDL

Un seul fichier DDL peut contenir plusieurs commandes qui, en raison d'une syntaxe correcte, s'exécuteront dans l'ordre et apporteront des modifications au schéma telles que la création de jeux de caractères et de tables, la suppression de tables, le renommage et la modification de tables. Les commandes DDL suivantes sont couramment utilisées lors de l'utilisation du schéma de base de données.

`CREATE` - Utilisé pour créer la base de données ou ses objets (comme une table, un index, une fonction, des vues, une procédure de stockage et des déclencheurs).

`DROP` - Utilisé pour supprimer des objets de la base de données.

`ALTER` - Utilisé pour modifier la structure de la base de données.

`TRUNCATE` - Utilisé pour supprimer tous les enregistrements d'une table, y compris tous les espaces alloués pour les enregistrements sont supprimés.

`COMMENT` – Ajoute des commentaires au dictionnaire de données.

`RENAME` - Renomme un objet existant dans la base de données.

## Exemple DDL

L'exemple suivant montre l'instruction DDL pour la commande CREATE qui crée une table et définit ses champs.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Références ##

* [DDL par Wikipédia](https://en.wikipedia.org/wiki/Data_definition_language)

