{
"date": "01/03/2023",
  "keywords": [
"fichier de puce",
"qu'est-ce qu'un fichier chip",
"déposer",
"comment ouvrir le fichier de la puce",
"extension de fichier de puce",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CHIP - Fichier d'annotation de micropuces",
  "description":"Découvrez le format de fichier CHIP et les API permettant de créer et d'ouvrir des fichiers CHIP.",
"linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
"parent" : "spreadsheet"
}
},
"derniermod": "01/03/2023"
}

## Qu'est-ce qu'un fichier CHIP ?

Le fichier CHIP est un fichier d'annotation de micropuces et est lié au logiciel Gene Set Enrichment Analysis (GSEA). La GSEA est une méthode informatique qui évalue si un ensemble prédéfini de gènes (un ensemble de gènes) présente des différences statistiquement significatives entre deux états biologiques, tels qu'un tissu sain par rapport à un tissu malade ou un traitement médicamenteux par rapport à des cellules non traitées. Pour effectuer la GSEA, vous avez besoin d’un ensemble de données d’expression génique et d’une base de données d’ensembles de gènes. La base de données d'ensembles de gènes contient des informations sur les gènes contenus dans les ensembles de gènes, telles que leur fonction, leur voie ou leur expression spécifique à un tissu.

Un fichier CHIP est un type spécifique de base de données d’ensembles de gènes utilisé par GSEA. Il contient des informations sur les gènes et les ensembles de gènes pertinents pour la plate-forme de puces à ADN utilisée dans l'expérience. Le fichier CHIP fournit des annotations pour chaque sonde de la puce à ADN, telles que le symbole du gène, le nom du gène, la description du gène et l'emplacement chromosomique. Ces informations sont utilisées pour faire correspondre les sondes avec les gènes de l'ensemble de données d'expression génique et pour les attribuer aux ensembles de gènes appropriés pour l'analyse GSEA.

Pour utiliser un fichier CHIP dans GSEA, vous devez l'importer dans le logiciel et le lier à votre ensemble de données de micropuces. GSEA prend en charge diverses plates-formes de puces à ADN et fournit des fichiers CHIP prédéfinis pour beaucoup d'entre elles. Cependant, vous pouvez également créer votre propre fichier CHIP à l'aide de bases de données d'annotations provenant de sources externes, telles que NCBI ou Ensembl.

## Plus d'information

Un fichier CHIP n'est pas une feuille de calcul, mais il peut être ouvert et modifié dans un tableur comme Microsoft Excel ou Google Sheets. Un fichier CHIP est un type de fichier texte contenant des données délimitées par des tabulations, qui peuvent être facilement importées dans un tableur pour être visualisées et modifiées.

Dans un tableur, vous pouvez manipuler les données d'un fichier CHIP pour ajouter, supprimer ou modifier des annotations pour les gènes et les ensembles de gènes sur la puce à ADN. Par exemple, vous pouvez utiliser un tableur pour ajouter des annotations personnalisées pour les gènes qui ne sont pas inclus dans le fichier CHIP d'origine, ou pour fusionner plusieurs fichiers CHIP provenant de différentes sources en un seul fichier.

Cependant, il est important de noter qu'un fichier CHIP a un format et une structure spécifiques qui doivent être conservés pour assurer la compatibilité avec le logiciel GSEA. Si vous modifiez le contenu d'un fichier CHIP dans un tableur, vous devez vous assurer que les modifications ne modifient pas le format ou le contenu du fichier d'une manière qui pourrait affecter l'exactitude ou la validité de l'analyse GSEA.

## Comment ouvrir le fichier CHIP?

Étant donné que le fichier CHIP contient des données délimitées par des tabulations, donc si vous souhaitez afficher les données de la feuille de calcul, vous pouvez l'ouvrir dans Microsoft Excel.

## Les références
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
