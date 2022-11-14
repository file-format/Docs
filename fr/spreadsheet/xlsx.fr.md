{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "fichier", "extension", "format de fichier", "Excel", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez ce qu'est un fichier XLSX et les API qui peuvent créer et ouvrir des fichiers XLSX.",
  "title" :"Format de fichier XLSX - Qu'est-ce qu'un fichier XLSX ?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier XLSX ?

**XLSX** est un format bien connu pour les documents Microsoft Excel qui a été introduit par Microsoft avec la sortie de Microsoft Office 2007. Basé sur une structure organisée selon les conventions d'emballage ouvertes comme indiqué dans la [Partie 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) de la norme OOXML ECMA-376, le nouveau format est un package zip contenant un certain nombre de fichiers XML. La structure et les fichiers sous-jacents peuvent être examinés en décompressant simplement le fichier .xlsx.

## Bref historique du format de fichier XLSX

Le format de fichier XLSX a été introduit en 2007 et utilise la norme Open XML adaptée par Microsoft en 2000. Avant XLSX, le format de fichier commun utilisé était [XLS](/fr/spreadsheet/xls/) qui était un format de fichier binaire pur. Le nouveau type de fichier a ajouté des avantages de petites tailles de fichiers, moins de changements de corruption et une représentation d'images bien formatées. C'est au début des années 2000 que Microsoft a décidé de changer pour s'adapter à la norme **Office Open XML**. En 2007, ce nouveau format de fichier a été intégré à Office 2007 et est également repris dans les nouvelles versions de Microsoft Office.

## Spécifications du format de fichier XLSX

Les [spécifications officielles du format de fichier XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) sont disponibles en ligne auprès de Microsoft. Afin de voir ce qu'il y a à l'intérieur du fichier XLSX, il suffit de le renommer en fichier [ZIP](/fr/compression/zip/) en modifiant son extension puis de l'extraire pour afficher les fichiers constitutifs de ce classeur Excel. Un classeur vide, lorsqu'il est extrait dans ses fichiers, contient les fichiers et dossiers constitutifs suivants.

### [Content_Types].xml ###

C'est le seul fichier qui se trouve au niveau de base lorsque le zip est extrait. Il répertorie les types de contenu pour les parties du package. Toutes les références aux fichiers XML inclus dans le package sont référencées dans ce fichier XML.

### \_rels (Dossier) ###

Il s'agit du dossier Relations qui contient un seul fichier XML qui stocke les relations au niveau du package. Les liens vers les parties clés des fichiers Xlsx sont contenus dans ce fichier sous forme d'URI. Ces URI identifient le type de relation de chaque partie clé avec le package. Cela inclut la relation avec le document Office principal situé en tant que xl/workbook.xml et d'autres parties dans docProps en tant que propriétés principales et étendues.

### docProps ###

Ce dossier contient les propriétés générales du document. Il s'agit notamment d'un ensemble de propriétés principales, d'un ensemble de propriétés étendues ou spécifiques à l'application et d'un aperçu miniature du document. Un classeur vide contient deux fichiers dans ce dossier, à savoir app.xml et core.xml. Le core.xml contient des informations telles que l'auteur, la date de création et d'enregistrement et de modification. App.xml contient des informations sur le contenu du fichier.

### xl (dossier) ###

Il s'agit du dossier principal qui contient tous les détails sur le contenu du classeur. Par défaut, il contient les dossiers suivants :

* \_rels
* thème
* des feuilles de calcul

et les fichiers xml suivants :

* styles.xml
* classeur.xml

## Exemple de format XLSX ##


Pour chaque feuille de calcul Excel contenue dans un classeur, il existe un fichier XML. Vous pouvez trouver ces fichiers XML dans le dossier xl/worksheets. Toutes les informations contenues dans une feuille de calcul sont organisées dans différentes sections du fichier XML. Examinons un exemple de feuille de calcul d'un classeur illustré dans l'image suivante.

{{< figure src="../XLSX file format.png" alt="Format de fichier XLSX" >}}

Comme on peut le voir, cette feuille de calcul contient le contenu des cellules A1 à B2 et une image. De plus, la cellule G13 est actuellement la cellule active dans la feuille de calcul. Maintenant, examinons le fichier xl/worksheets/sheet1.xml pour voir comment ces informations sont représentées dans le fichier XML. Le contenu de ce fichier XML est illustré ci-dessous.

{{< figure src="../XLSX File Format Details.png" alt="Format de fichier XPS" >}}

1. L'onglet a une couleur de thème qui lui est appliquée. Il est mentionné dans le fichier XML avec la balise<tabColor> suivant l'identifiant du thème.
1. La valeur tabSelected est définie sur 1, ce qui indique qu'il s'agit de la feuille sélectionnée
1. Comme on peut le voir dans la première image ci-dessus, la cellule G13 de la feuille de calcul est une cellule active qui est également mentionnée dans le fichier XML.
1. L'onglet sheetData représente les données contenues dans la feuille de calcul. Cependant, vous pouvez voir que le contenu original de la feuille de calcul ne se trouve nulle part dans cette section. En effet, le texte est indirectement référencé à partir de la feuille XML "sharedStrings". Cette liaison garantit que chaque texte n'est enregistré qu'une seule fois et peut être référencé à nouveau afin d'économiser de l'espace.
1. L'image comme on peut le voir est référencée par l'identifiant de référence "rId2"

## Contribuer

Vous devez partager quelque chose sur les formats de fichier XLSX ou Spreadsheet ? Vous pouvez publier vos résultats dans la section [Nouvelles sur le format de fichier de feuille de calcul](https://news.fileformat.com/t/Spreadsheet).

## Références

* [[MS-XLSX] - Format de fichier XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML] (http://officeopenxml.com/anatomyofOOXML-xlsx.php)

