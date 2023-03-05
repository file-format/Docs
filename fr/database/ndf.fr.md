{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MDF et les API qui peuvent créer et ouvrir des fichiers NDF.",
  "title" :"Format de fichier NDF - Fichier de base de données principale SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier NDF ?

Un fichier avec l'extension .ndf est un fichier de base de données secondaire utilisé par [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) pour stocker les données utilisateur. NDF est un fichier de stockage secondaire car le serveur SQL stocke les données spécifiées par l'utilisateur dans un fichier de stockage principal appelé [MDF](/fr/database/mdf/). Le fichier de données NDF est facultatif et défini par l'utilisateur pour gérer le stockage des données au cas où le fichier MDF principal utiliserait tout l'espace alloué. Il est généralement stocké sur un disque séparé et peut se propager sur plusieurs périphériques de stockage. La présence de fichiers MDF est nécessaire pour ouvrir les fichiers NDF.

## Format de fichier NDF

Le format de fichier NDF n'est pas différent de [MDF](/fr/database/mdf) et utilise les pages comme unité fondamentale de stockage de données. chaque page commence par un en-tête de 96 octets qui comprend :

* Identifiant de la page
*Type d'ouvrage
* Nombre d'enregistrements dans les pages
* Pointeurs vers les pages précédentes et suivantes

### Structure du fichier NDF

Un fichier MDF a la structure de données suivante.

* Page 0 : En-tête
* Page 1 : Premier PSF
* Page 2 : Premier GAM
* Page 3 : Premier SGAM
*Page 4 : Inutilisé
*Page 5 : Inutilisé
* Page 6 : Premier DCM
* Page 7 : Premier BCM

#### En-tête de fichier NDF

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

## Page Fichier de données

Les pages d'un fichier de données SQL Server commencent à zéro (0) et s'incrémentent de manière séquentielle. Chaque fichier est reconnu par un numéro d'identification de fichier unique. La paire d'ID de fichier et de numéro de page identifie de manière unique une page dans une base de données. Un exemple montrant les numéros de page dans une base de données, est comme dans l'image suivante.

{{< figure src="../ndf.png" alt="Format de fichier de base de données NDF" >}}

Cet exemple montre les numéros de page dans une base de données qui a un fichier de données principal de 4 Mo et un fichier de données secondaire de 1 Mo.

## Références

* [Fichiers de base de données et groupes de fichiers](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Détacher et attacher la base de données - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analyse de l'anatomie du fichier de données SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

