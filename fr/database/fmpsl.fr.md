{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier FMPSL et les API qui peuvent créer et ouvrir des fichiers FMPSL.",
  "title" :"Format de fichier FMPSL - Fichier de lien d'instantané FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Qu'est-ce qu'un fichier FMPSL ?

Un fichier FMPSL est un fichier d'instantané de base de données créé avec FileMaker Pro 12. Il stocke les résultats interrogés de la base de données avec d'autres informations telles que la disposition visuelle et les informations visibles. Le fichier FMPSL peut être utilisé pour restaurer toutes ces données dans une autre instance de la base de données FileMaker Pro. Ce format de fichier a été introduit avec le lancement de FileMaker Pro v 12. Avant cette version, les liens d'instantanés étaient introduits au format de fichier FPSL dans FileMaker Pro v 11. Les fichiers FMPSL peuvent être ouverts avec le logiciel FileMaker Pro Advanced. Les autres formats de fichiers pris en charge par FileMaker Pro incluent [FP5](/fr/database/fp5/), [FP7](/fr/database/fp7/) et [FMP12](/fr/database/fmp12/).

## Format de fichier FMPSL

Les détails du format de fichier interne des fichiers FMPSL ne sont pas disponibles publiquement pour la référence du développeur.

### Comment enregistrer des enregistrements en tant que fichier FMPSL ?

Les données de la base de données FileMaker Pro peuvent être enregistrées en tant que fichier de lien d'instantané en procédant comme suit.

1. Recherchez les enregistrements de la base de données qui doivent être enregistrés en tant que fichier de lien d'instantané.
1. À l'aide de l'option Envoyer l'enregistrement en tant que lien d'instantané du menu, enregistrez le fichier en saisissant un nom de fichier.
1. Utilisez les enregistrements parcourus pour enregistrer l'ensemble des enregistrements trouvés.

Le fichier d'instantané généré sera enregistré sur le disque avec le nom spécifié.

## Références

* [Convertir les versions antérieures des formats de fichiers FileMaker Pro au format de fichier FMP12] (https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Enregistrer les enregistrements en tant que fichier de lien d'instantané] (https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

