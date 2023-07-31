{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier ADE et les API qui peuvent créer et ouvrir des fichiers ADE.",
  "title" :"ADE - Accéder au fichier d'extension de projet",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Qu'est-ce qu'un fichier ADE ?

Un fichier avec l'extension .ade est un fichier de projet Microsoft Access qui contient la sortie compilée des informations contenues dans le fichier de projet Microsoft Access ADP. Les informations contenues dans le fichier de projet Access, autres que Visual Basic pour Applications (VBA), sont disponibles sous forme compilée dans les fichiers ADE. Les données sont stockées au format compressé dans ces fichiers pour réduire la taille du fichier et améliorer les performances dans Access. Étant donné qu'ADE est la sortie compilée du fichier de projet Access, tout code source VBA faisant partie du projet reste protégé en ne lui permettant pas de faire partie de la sortie. Les fichiers ADE peuvent être ouverts dans Microsoft Access 365.

## Format de fichier ADE - Plus d'informations

ADE sont des fichiers de base de données Access compilés qui sont stockés sur disque sous forme de fichiers binaires. La structure de fichier interne de ces fichiers n'est pas connue.

Les fichiers ADE peuvent créer des problèmes d'ouverture en fonction de la version de Microsoft Access qui a été utilisée pour créer ces fichiers. Les bases de données Access qui utilisent la version 64 bits de Microsoft Access 2010 et qui sont compilées en tant que fichiers MDE, [ACCDE](/fr/database/accde/) ou ADE doivent être recompilées dans Microsoft Access 2021 Service Pack 1 (SP1) pour fonctionnent correctement avec Access 2010 SP1. Ce problème se produit car Access 2010 SP1 utilise une version plus récente du fichier VBE7.dll (version 7.00.1619).

## Références

* [Problème avec les fichiers Access ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Quels formats de fichiers d'accès utiliser](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

