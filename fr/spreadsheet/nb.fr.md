{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "fichier", "extension", "format de fichier", "Mathematica", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Découvrez ce qu'est une API de fichier NB qui peut créer et ouvrir des fichiers NB.",
  "title" :"NB - Format de fichier de bloc-notes Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Qu'est-ce qu'un fichier NB ?

Un fichier avec l'extension .nb est un format de fichier de bloc-notes Wolfram qui enregistre les instructions pour les instructions mathématiques dans un fichier texte. Il peut contenir de nombreux types de données différents, tels que des calculs en direct, des interfaces dynamiques arbitraires, une entrée de composition complète, une entrée d'image, une annotation de code automatique, une interface de programmation complète de haut niveau et des milliers de fonctions et d'options soigneusement organisées. Les instructions textuelles sont des entrées et des sorties Mathematica qui sont générées et mises à jour au fur et à mesure que les instructions d'entrée sont placées dans le fichier.

## Format de fichier Wolfram Notebook NB - Plus d'informations

Les fichiers Wolfram Notebook NB sont enregistrés au format texte brut, qui est un format de fichier lisible par l'homme. Le contenu d'un bloc-notes est organisé en sections sous forme de texte brut, chacune étant représentée par des groupes de cellules, similaires à une feuille de calcul. La plage de ces groupes est définie par une parenthèse vers la fin de chaque cellule. Le style attribué à une cellule détermine son rôle dans le bloc-notes, comme détaillé ci-dessous.

### Notebooks en Wolfram Language

Lorsqu'il est prévu d'enregistrer le Notebook composé d'instructions mathématiques à exécuter par Wolfram Language Kernal, les cellules du document se voient automatiquement attribuer le style de texte "Entrée". Cela indique au noyau de les considérer comme des instructions exécutées lorsque l'utilisateur émet une combinaison de touches `Shift + Return`. Un cahier Mathematica est comme illustré dans l'exemple suivant.

{{< figure src="../Wolfram Notebook.jpeg" alt="Format de fichier du bloc-notes Wolfram" >}}

### Blocs-notes en tant que documents

Les cahiers Mathematica peuvent être au format document pour donner un aperçu de ce que vous voyez et de ce que vous obtenez (WYSIWYG). Ces documents sont les mêmes que ceux visualisés à l'écran ou sur papier imprimé, et sont interactifs. Pour cela, le `Style de texte` est attribué à la cellule pour afficher le contenu sans exécuter les instructions par le noyau.

## Exporter des cahiers Mathematica

Les cahiers Mathematica peuvent être exportés vers de nombreux formats de fichiers différents tels que PDF, graphiques, SIG, compressés et feuilles de calcul.

## Références

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)

