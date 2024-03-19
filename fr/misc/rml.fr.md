{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Fichier de modèle de rapport Elixir",
  "description":"En savoir plus sur le fichier RML et les API qui peuvent créer et ouvrir des fichiers RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Qu'est-ce qu'un fichier RML ?

Un fichier RML est un fichier de modèle de rapport avec le moteur de rapport [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Le fichier modèle est utilisé pour générer des rapports avec la source de données connectée au système de fichiers Elixir. Les données sont lues et remplies dans le fichier de modèle RML et peuvent être exportées vers un certain nombre de formats de fichiers différents tels que [PDF](/fr/pdf/), [RTF](/fr/word-processing/rtf/) et tableur [XLS](/fr/spreadsheet/xls/). Le moteur de reporting Elixir Repertoire peut être connecté à une grande variété de sources de données JDBC.

## Format de fichier RML

Les détails de la structure de fichier interne du format de fichier RML ne sont pas disponibles publiquement. Les fichiers sont générés et enregistrés en interne par l'application Elixir Repertoire pour générer des rapports avec des données renseignées à partir des sources de données connectées. Le fichier de modèle RML contient la mise en page globale et les informations d'espace réservé du rapport final à générer à partir des données.

## Comment créer un fichier de modèle RML ?

Afin de générer un modèle RML dans Elixir Repertoire, les étapes suivantes peuvent être suivies.

1. Connectez une source de données JDBC au système de fichiers.
1. Lancez l'assistant de modèle de rapport
1. Utilisez le logiciel pour localiser le fichier .ds de la source de données
1. Choisissez le rapport tabulaire comme choix d'exportation
1. Sélectionnez les champs à inclure dans le modèle de rapport
1. Enfin, en cliquant sur le bouton Terminer, First report.rml est ajouté au référentiel et ouvert pour afficher l'onglet Mise en page.

## Références

* [Répertoire Elixir](https://elixirtech.com/repertoire-2/)

