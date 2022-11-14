{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier ACCDT et les API qui peuvent créer et ouvrir des fichiers ACCDT.",
  "title" :"ACCDT - Format de fichier de base de données de modèles Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Qu'est-ce qu'un fichier ACCDT ?

Un fichier avec l'extension .accdt est un fichier de modèle de base de données Microsoft Access qui contient des éléments de base de données prédéfinis. Ces éléments sont un ensemble de structures qui définissent des applications de base de données telles que des schémas de base de données pour stocker des données, une description de mise en page pour les vues des données et des métadonnées décrivant la base de données. En tant que fichiers de modèle, les fichiers ACCDT peuvent être utilisés pour créer des bases de données basées sur les paramètres de modèle disponibles dans ceux-ci. Les fichiers de base de données résultants sont enregistrés en tant que fichiers [ACCDB](/fr/database/accdb/) et remplis de données dans des tables. Microsoft Access 2007 et versions ultérieures peuvent ouvrir les fichiers ACCDT.

## Format de fichier ACCDT

Les fichiers de modèle ACCDT sont basés sur les spécifications Office Open XML et toutes les données sont contenues dans un package ZIP. Les informations sur la structure et le contenu de la base de données sont contenues dans les fichiers [XML](/fr/web/xml/) et les fichiers texte et sont liées les unes aux autres via des relations. Vous pouvez renommer un fichier ACCDT en extension [.zip](/fr/compression/zip/) et utiliser n'importe quel logiciel de compression pour extraire le contenu de l'archive ZIP.

### Structure du fichier

Les fichiers ACCDT sont des packages qui contiennent une collection de pièces associées. Chaque **partie** stocke des informations sur le contenu d'une application de base de données à l'aide de formats XML, texte et binaire, notamment :

* Objets de base de données
* Métadonnées associées
* Structure du forfait

#### Forfait

Un package est une archive [ZIP](/fr/compression/zip/) qui contient plusieurs parties et est conforme aux conventions d'emballage ouvertes spécifiées dans [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). Les fichiers ACCDT doivent contenir au moins une partie de métadonnées de modèle qui doit être la cible d'une relation. Ce modèle de métadonnées est la partie de départ d'un fichier ACCDT.

#### Partie

Une partie est un flux d'octets qui a un type associé pour spécifier la nature et le type de contenu qui y est stocké. L'énumération des parties spécifie les parties valides, les types de contenu valides et les relations requises entre toutes les parties d'un package.

#### Relation

`Package Relationship` - où la cible est une partie et la source est le package dans son ensemble.

`Relation partie à partie` - où la cible est une partie et la source est une partie du package.

`Relation explicite` - où une ressource est référencée à partir du contenu d'une partie source en référençant un élément de relation par la valeur de son attribut ID.

`Relation implicite` - une relation qui n'est pas explicite.

`Relation interne` - où la cible est une partie du package.

`Relation externe` - où la cible est une ressource externe ne figurant pas dans le package.

## Références ##

* [Format de fichier de modèle d'accès] (https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

