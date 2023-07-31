{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MDF et les API qui peuvent créer et ouvrir des fichiers MDF.",
  "title" :"Format de fichier MDF - Fichier de base de données maître SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier MDF ?

Un fichier avec l'extension .mdf est un fichier de base de données principal utilisé par [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) pour stocker les données utilisateur. C'est d'une importance primordiale car toutes les données sont stockées dans ce fichier. Le fichier MDF stocke les données des utilisateurs dans des bases de données relationnelles sous forme de colonnes, de lignes, de champs, d'index, de vues et de tables. SQL Server permet de définir les paramètres de croissance automatique et de réduction automatique pour avoir un impact positif sur les performances de la base de données. Les fichiers MDF peuvent être chargés et attachés à une base de données à l'aide de Microsoft SQL Server. Les fichiers MDF ont le type mime Application/octet-stream.

## Format de fichier MDF

L'unité fondamentale de stockage de données dans SQL Server est une page. Une page de stockage attribuée à la base de données est divisée en pages logiques numérotées de 0 à n. Une seule page commence par un en-tête de 96 octets qui comprend l'ID de page, le type de structure auquel appartient la page, le nombre d'enregistrements dans la page et des pointeurs vers les pages précédentes et suivantes.

### Structure du fichier

Un fichier MDF a la structure de données suivante.

* Page 0 : En-tête
* Page 1 : Premier PSF
* Page 2 : Premier GAM
* Page 3 : Premier SGAM
*Page 4 : Inutilisé
*Page 5 : Inutilisé
* Page 6 : Premier DCM
* Page 7 : Premier BCM

#### En-tête de fichier

Le numéro de page 0 de tous les fichiers contient un en-tête qui stocke des métadonnées sur le fichier.

#### Espace libre de page (PFS)
PFS identifie le statut d'allocation et détermine la quantité d'espace libre.

* Bit 1 : Indique si la page est allouée ou non.
* Bit 2 : Indique si la page provient d'une étendue mixte.
* Bit 3 : Indique que cette page est une page IAM.
* Bit 4 : Indique que cette page contient des enregistrements fantômes
* Bits 5 à 7 : une valeur combinée de trois bits, qui indique le remplissage de la page comme suit :
* 0 : La page est vide
* 1 : La page est pleine de 1 à 50 %
* 2 : La page est pleine à 51–80 %
* 3 : La page est pleine à 81–95 %
* 4 : La page est pleine à 96–100 %

## Références

* [Fichiers de base de données et groupes de fichiers](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Détacher et attacher la base de données - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analyse de l'anatomie du fichier de données SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

