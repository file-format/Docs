{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "fichier", "extension", "format de fichier", "Macro Excel Open XML", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier XLTM et les API qui peuvent les créer et les ouvrir.",
  "title" :"Qu'est-ce qu'un fichier XLTM ?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier XLTM ?

L'extension de fichier XLTM représente les fichiers générés par Microsoft Excel en tant que fichiers de modèle prenant en charge les macros. Les fichiers XLTM sont similaires à [XLTX](/fr/spreadsheet/xltx/) dans leur structure, sauf que ce dernier ne prend pas en charge la création de fichiers modèles avec des macros. Ces fichiers modèles sont utilisés pour générer et définir la mise en page, le formatage et d'autres paramètres ainsi que les macros pour faciliter la création de fichiers XLSX similaires.

## Bref historique ##

C'est au début des années 2000 que Microsoft a décidé de changer pour s'adapter à la norme **Office Open XML**. Les documents, de différents types, sous cette nouvelle norme ont été identifiés en ajoutant "X" dans leurs extensions, "X" étant pour XML. En 2007, ce nouveau format de fichier a été intégré à Office 2007 et est également repris dans les nouvelles versions de Microsoft Office. Le nouveau type de fichier a ajouté des avantages de petites tailles de fichiers, moins de changements de corruption et une représentation d'images bien formatées.

## Spécifications du format de fichier XLTM ##

Les fichiers XLTM sont basés sur le format de fichier Office OpenXML et utilisent XML et [ZIP](/fr/Compression/ZIP/) pour réduire la taille du fichier. Ceux-ci peuvent être ouverts avec Microsoft Excel en double-cliquant sur le fichier. L'organisation des fichiers dans un format de fichier XLTM peut être observée en renommant le fichier en ZIP, puis en extrayant son contenu sur le disque.

### [Content_Types].xml ###

C'est le seul fichier qui se trouve au niveau de base lorsque le zip est extrait. Il répertorie les types de contenu pour les parties du package. Toutes les références aux fichiers XML inclus dans le package sont référencées dans ce fichier XML.

### \_rels (Dossier) ###

Il s'agit du dossier Relations qui contient un seul fichier XML qui stocke les relations au niveau du package. Les liens vers les éléments clés des fichiers Xltx sont contenus dans ce fichier sous forme d'URI. Ces URI identifient le type de relation de chaque partie clé avec le package. Cela inclut la relation avec le document de bureau principal situé en tant que xl/workbook.xml et d'autres parties dans docProps en tant que propriétés étendues et étendues.

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

## Références ##

* [Format de fichier MS-XLSX](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

