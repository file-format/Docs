{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MDB et les API qui peuvent créer et ouvrir des fichiers MDB.",
  "title" :"Format de fichier MDB - Un fichier de base de données Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Qu'est-ce qu'un fichier MDB ?

Un fichier avec l'extension .mdb est un fichier de base de données Microsoft Access qui est un système de gestion de base de données relationnelle (RDBMS). Il stocke les données dans des tables de base de données qui sont liées les unes aux autres via des clés primaires et étrangères. Le fichier MDB contient la structure complète des tables de la base de données, des requêtes et des procédures stockées. MDB est le format de fichier par défaut pour Microsoft Access 2003. Les versions latérales de Microsoft Access utilisent les formats de fichier [ACCDB](/fr/database/accdb/) qui est le dernier format de fichier à ce jour. Les fichiers MDB peuvent être ouverts avec des applications telles que Microsoft Access, MDB Viewer, MDBOpener et peuvent être convertis en formats ACCDB, [CSV](/fr/spreadsheet/csv/), Excel, etc.

## Format de fichier MDB

Il existe des spécifications publiques disponibles pour le format MDB et il reste le format de fichier propriétaire de Microsoft. Cependant, Microsoft fournit un accès de connectivité au fichier MDB à l'aide de la norme ODBC (Open Database Connectivity) et de Visual Basic pour Applications (VBA). Le guide MDB non officiel fournit une brève description informelle du format MDB basé sur l'ingénierie inverse et peut être consulté pour connaître les spécifications.

###Pages

Selon le guide MDB non officiel, un fichier MDB se compose de pages de taille fixe (2048 octets pour Jeb DB3 et 4096 octets pour Jet DB 4). Le premier octet indique le type de page. Voici les principaux types de pages :

`First Page:` Il contient des informations d'en-tête de base de données qui incluent également l'identification de la version Jet DB avec laquelle le fichier est compatible. En outre, il comprend également des informations sur la sécurité des fichiers et une carte d'utilisation des pages.

`Page de définition de table :` Une page de définition de table spécifie les colonnes, les types de données, l'index et d'autres informations. Il utilise des pages supplémentaires si nécessaire et inclut une carte de pages qui contient les données de ligne pour cette table.

`Pages de données :` Les pages de données sont les véritables conteneurs de données où les données sont stockées par lignes. Il utilise des pages subsidiaires pour stocker de longues valeurs de données.

Une seule base de données Microsoft Access peut comprendre plusieurs fichiers qui permettent de dépasser les limites de taille de fichier et de table. Cela facilite le placement des formulaires et du code dans un fichier MDB frontal sur le bureau de l'utilisateur et des données dans un autre fichier MDB principal sur des serveurs connectés au réseau.

## Références ##

* [Spécifications d'accès](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Le guide MDB non officiel](http://jabakobob.net/mdb/)

