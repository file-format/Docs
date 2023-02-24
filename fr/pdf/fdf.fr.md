{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier FDF - Qu'est-ce qu'un fichier FDF ?",
  "description":"En savoir plus sur le format de fichier FDF et les API qui peuvent créer et ouvrir des fichiers FDF.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier FDF ?

Un fichier FDF (**Forms Data Format**) est un document texte généré en exportant des données à partir des champs de formulaire d'un fichier [PDF](/fr/pdf/). Il inclut uniquement les données des champs de texte extraites des champs de formulaire disponibles dans un fichier PDF. Cela se traduit par un fichier de données relativement petit car les données exportées ne contiennent pas le formulaire lui-même. Adobe Acrobat fournit la fonctionnalité d'exportation des données des champs de formulaire en utilisant l'option "Exporter les données des formulaires" dans le menu de l'application.

## Format de fichier FDF - Plus d'informations

FDF est un format de texte brut et fait partie de la [norme ISO 32000](https://www.iso.org/standard/51502.html) pour le format de document portable. Il a été développé par Adobe pour permettre l'importation et l'exportation de données à partir d'Acrobat Forms ou d'AcroForms.

Il existe deux types de fichiers FDF :

• `Classic FDF` - Il fournit des données pour remplir un formulaire statique existant.

• `Template FDF` - Construit un nouveau PDF basé sur des modèles à partir de fichiers PDF spécifiés. Les formulaires à l'intérieur du nouveau document sont remplis en fournissant des données.

## Création de FDF avec Adobe Acrobat

La [boîte à outils FDF](https://opensource.adobe.com/dc-acrobat-sdk-docs/) d'Adobe vous permet de créer des fichiers FDF à partir de données textuelles.

## Références ##

* [Prise en charge du format FDF par Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Ressources pour les développeurs Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)
