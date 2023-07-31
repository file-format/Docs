{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "fichier", "extension", "format de fichier", "Fichier macro Microsoft Excel", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier de macros XLM et les API qui peuvent créer et ouvrir des fichiers XLM.",
  "title" :"Qu'est-ce qu'un fichier XLM ?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier XLM ?

XLM, pour Excel Macro, est un type de fichier de feuille de calcul utilisé pour stocker des macros. Du point de vue de l'application, une macro est un ensemble d'instructions utilisées pour automatiser les processus. Une macro est utilisée pour enregistrer les étapes qui sont exécutées à plusieurs reprises pour le format de fichier [XLS](/fr/spreadsheet/xls/) et facilite l'exécution des actions en exécutant à nouveau la macro. Les macros sont programmées avec Visual Basic pour Applications (VBA) de Microsoft à partir du classeur Excel à l'aide de Visual Basic Editor et peuvent être exécutées/déboguées directement à partir de là.

## Bref historique ##

Microsoft Excel a pris en charge la programmation de macros depuis son premier lancement public. Les fonctionnalités des macros sont restées les mêmes dans les versions ultérieures d'Excel avec extension selon les nouvelles fonctionnalités. XLM était le langage macro par défaut pour Excel jusqu'à Excel 4.0. Excel 5.0 enregistrait les macros dans VBA par défaut, mais avec la version 5.0, l'enregistrement XLM était toujours autorisé en option. Après la version 5.0, cette option a été abandonnée. Toutes les versions d'Excel, y compris Excel 2010, sont capables d'exécuter une macro XLM, bien que Microsoft déconseille leur utilisation.

## Enregistrer une macro en XLM ##

Excel fournit des étapes faciles à utiliser pour enregistrer une macro. Il nécessite que vous ayez installé les outils de développement pour travailler avec les macros. Une fois qu'un enregistrement de macro est en cours, il enregistre chaque action de l'utilisateur pour être jouée plus tard. L'enregistrement de macro implique en fait toutes les étapes qu'un utilisateur effectue après le début de l'enregistrement. Ainsi, si vous mettez le contenu d'une cellule en gras, en italique et définissez sa justification de texte après le démarrage d'un enregistrement de macro, toutes ces commandes seront enregistrées. Chaque macro enregistrée peut également être associée à un raccourci pour une lecture rapide ultérieurement. L'enregistrement de macro génère du code VBA sous la forme d'une macro qui peut être modifiée à l'aide de Visual Basic Editor (VBE).

## Modèle d'objet Excel ##

Les macros utilisent des routines VBA dans leur dos et suivent le [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) à cette fin. Ce modèle identifie les objets d'une feuille de calcul pour une interaction avec la feuille de calcul via des barres d'outils de commandes définies par l'utilisateur, des barres de commandes ou des boîtes de messages. Par exemple, l'accès aux propriétés du classeur est accordé avec l'objet Workbook. De même, il existe un objet Worksheet dans le modèle pour travailler avec les feuilles de calcul du classeur par programmation.

## Macros et sécurité ##

VBA permet d'accéder à tous les domaines d'application ainsi qu'au système de fichiers et peut également être dangereux. Cela soulève des inquiétudes lors du partage du classeur avec quelqu'un qui peut exécuter le fichier de son côté. C'est-à-dire que Microsoft Excel met en garde contre l'ouverture d'un tel fichier. Les macros peuvent être certifiées avec une signature numérique afin que d'autres utilisateurs puissent vérifier qu'elles sont dignes de confiance. Ainsi, les macros peuvent être activées après vérification de leur source.

## Références ##

* [[MS-XLS] - Structure du format de fichier binaire Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programmation de macros](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

