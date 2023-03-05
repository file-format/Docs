{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier _XLSX et les API qui peuvent créer et ouvrir des fichiers _XLSX.",
  "title" :"Qu'est-ce qu'un fichier _XLSX ?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Qu'est-ce qu'un fichier _XLSX ?

Un fichier avec l'extension .\_xlsx est en fait un fichier [XLSX](/fr/spreadsheet/xlsx/) renommé par une autre application. Cela peut arriver dans certains cas lorsque le nom de fichier contient un . à la fin du nom du fichier. Les fichiers \_XLSX peuvent être ouverts dans Microsoft Excel de la même manière que les fichiers XLSX en les renommant à nouveau en extension .xlsx.

## _Format de fichier XLSX - Plus d'informations

Les fichiers _XLSX ne sont pas différents des fichiers XLSX et utilisent la norme Open XML adoptée par Microsoft en 2000. Avant XLSX, [XLS](/fr/spreadsheet/xls/) était le principal format de fichier utilisé pour travailler avec des feuilles de calcul Excel pour enregistrer des documents. au format binaire. Ce nouveau format de fichier basé sur XML présentait des avantages tels que la petite taille des fichiers, la résistance à la corruption des fichiers et la représentation d'images bien formatées. Ce nouveau format de fichier basé sur XML est devenu une partie d'Office 2007 et est également exécuté dans les nouvelles versions de Microsoft.

## \_Spécifications du format de fichier XLSX

Comme un fichier \_XLSX est un fichier XLSX renommé, il a les mêmes spécifications que le fichier d'origine. Il s'agit simplement d'un fichier d'archive basé sur le format de fichier d'archive [ZIP](/fr/compression/zip/). Si vous souhaitez voir le contenu de cette archive, renommez simplement le fichier en extension .zip et extrayez-le pour afficher les fichiers constitutifs de ce classeur Excel. Un classeur vide, lorsqu'il est extrait dans ses fichiers, contient les fichiers et dossiers constitutifs suivants.

### [Content_Types].xml

C'est le seul fichier qui se trouve au niveau de base lorsque le zip est extrait. Il répertorie les types de contenu pour les parties du package. Toutes les références aux fichiers XML inclus dans le package sont référencées dans ce fichier XML.

### \_rels (Dossier)

Il s'agit du dossier Relations qui contient un seul fichier XML qui stocke les relations au niveau du package. Les liens vers les parties clés des fichiers Xlsx sont contenus dans ce fichier sous forme d'URI. Ces URI identifient le type de relation de chaque partie clé avec le package. Cela inclut la relation avec le document Office principal situé en tant que xl/workbook.xml et d'autres parties dans docProps en tant que propriétés principales et étendues.

### docProps

Ce dossier contient les propriétés générales du document. Il s'agit notamment d'un ensemble de propriétés principales, d'un ensemble de propriétés étendues ou spécifiques à l'application et d'un aperçu miniature du document. Un classeur vide contient deux fichiers dans ce dossier, à savoir app.xml et core.xml. Le core.xml contient des informations telles que l'auteur, la date de création et d'enregistrement et de modification. App.xml contient des informations sur le contenu du fichier.

### xl (dossier)

Il s'agit du dossier principal qui contient tous les détails sur le contenu du classeur. Par défaut, il contient les dossiers suivants :

* \_rels
* thème
* des feuilles de calcul

et les fichiers xml suivants :

* styles.xml
* classeur.xml

## Références

* [MS-XLSX - Format de fichier .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

