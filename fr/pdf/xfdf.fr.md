{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier XFDF - Qu'est-ce qu'un fichier XFDF ?",
  "description":"En savoir plus sur le fichier XFDF et les API qui peuvent créer et ouvrir des fichiers XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier XFDF ?

Un fichier avec l'extension .xfdf est un format de données de formulaires XML généré avec le logiciel Adobe Acrobat. Comme [FDF](/fr/pdf/fdf/), XFDF contient la description des éléments de formulaire et leurs valeurs au format XML. Cela peut inclure les noms et les valeurs des champs de texte dans le formulaire PDF. Les XFDF sont enregistrés dans un format lisible par l'homme et peuvent être lus par programmation à l'aide de langages de programmation tels que C#.

## Format de fichier XFDF - Plus d'informations

Les fichiers XFDF sont enregistrés au format de fichier XML qui est un format universel utilisé pour l'importation et l'exportation de données. Une structure de fichier XFDF se compose d'un en-tête, suivi de valeurs de champ et de données d'éléments, comme indiqué ci-dessous.

|Élément|Attribut|Contenu|
---|---|---|
|\<XFDF> ||Élément supérieur|
|\<fields> ||Toutes les valeurs des champs pour ce modèle|
|<field (T)> |nom |Nom du champ|
|<value (V)> |valeur |Valeur du champ|

## Références

* [Prise en charge du format FDF par Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Ressources pour les développeurs Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

