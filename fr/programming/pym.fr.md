---
date: 2022-05-09
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fichier PYM - Fichier de préprocesseur de macro PYM
linktitle: PYM
description: "Découvrez le format de fichier PYM et les API qui peuvent créer et ouvrir des fichiers PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Qu'est-ce qu'un fichier PYM ?

Un fichier PYM est un fichier de préprocesseur de macro basé sur le langage de programmation Python. Il a été développé par VRVis Research et stocke des raccourcis de macros. Lorsque le fichier PYM est interprété par l'étape de prétraitement de l'interpréteur Python, ces raccourcis sont développés en remplacement de leur texte intégral. De plus, une troisième opération facultative qui peut être effectuée par un préprocesseur de macro est l'inclusion de fichiers. Les fichiers PYM peuvent être ouverts dans des éditeurs de texte tels que Notepad, Notepad++, Apple TextEdit et VI sous Linux.

## Format de fichier PYM

Les fichiers PYM sont enregistrés sous forme de fichiers texte brut sur le disque. Un fichier PYM peut également inclure d'autres fichiers en utilisant la directive `#include`.

### Syntaxe PYM

Les instructions PYM sont incluses entre les marqueurs "" #begin python et "#end python", comme indiqué ci-dessous.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Extension de macros PYM

L'extension de la macro PYM est représentée par deux séquences, c'est-à-dire <[ et ]>. Ce sont des balises html spéciales qui peuvent apparaître n'importe où sur une ligne. Un petit exemple PYM est le suivant.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Le résultat de l'exécution de ceci via PYM est le suivant :

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Références ##

* [PYM - Un préprocesseur de macros basé sur Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Interprètes PYM](https://github.com/interpreters/pym)

