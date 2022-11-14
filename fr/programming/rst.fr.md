{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier RST - Fichier texte restructuré",
  "description":"En savoir plus sur le format de fichier RST et les API qui peuvent créer et ouvrir des fichiers RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Qu'est-ce qu'un fichier RST ?

Un fichier RST est un format de fichier de documentation technique, utilisé principalement dans la communauté de programmation Python. Il s'agit d'un fichier texte écrit dans le langage de balisage reStructuredText qui applique des styles et une mise en forme aux documents en texte brut pour la génération de documentation. Les fichiers RST utilisent les commentaires et autres informations du code des programmes Python pour créer la documentation technique de l'application. Cependant, ceux-ci peuvent également contenir du texte pouvant être converti en pages Web simples et en [eBooks](/fr/ebook/). Les éditeurs de texte tels que Github Atom, GNU Emacs (multiplateforme), Microsoft Notepad (Windows), Apple TextEdit (Mac) et Vim (Linux) peuvent être utilisés pour ouvrir les fichiers RST.

## Format de fichier RST

Les fichiers RST contiennent du code écrit en langage de balisage reStructuredText. Il fait partie du projet Docutils de Python Doc-SIG (Documentation Special Interest Group) qui fournit un ensemble d'outils pour Python similaires à Javadoc pour Java. L'analyseur pour le format de fichier RST est intégré dans les Docutils et peut extraire des informations des programmes Python pour les formater dans la documentation du programme.

### Exemple RST reStructuredText

Prenons un exemple de texte écrit au format de fichier RST comme suit.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Lorsque ce texte est entré dans un processeur rST tel que Docutils, la sortie est la suivante.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Référence ##

* [reStructuredText - par Wikipédia](https://en.wikipedia.org/wiki/ReStructuredText)

