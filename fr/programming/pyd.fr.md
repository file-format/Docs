---
date: 2022-05-09
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fichier PYD - Module dynamique Python
linktitle: PYD
description: "Découvrez le format de fichier PYD et les API qui peuvent créer et ouvrir des fichiers PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Qu'est-ce qu'un fichier PYD ?

Un fichier PYD est une bibliothèque de liens dynamiques écrite en Python qui peut être exécutée par un autre code Python au moment de l'exécution. Il contient un ou plusieurs modules Python qui facilitent la réutilisation du code et fournissent une architecture de module pour l'écriture d'applications. Les fichiers PYD peuvent être créés et enregistrés avec l'extension .pyd, par exemple helloworld.pyd. Les développeurs d'applications peuvent utiliser l'instruction d'importation pour inclure les modules PYD dans leurs applications. Les fichiers PYD peuvent être ouverts avec Python Software Foundation Python qui est disponible pour les systèmes d'exploitation Windows, Mac et Linux.

## Format de fichier PYD - Plus d'informations

Les fichiers PYD sont écrits en langage de programmation Python et sont générés en compilant le code Python.

## Différence entre les formats de fichier PY et PYD

Un fichier [PY](/fr/programming/py/) contient du code source qui est exécuté tel quel et ne peut pas être inclus en tant que code réutilisable dans d'autres applications Python. Cependant, un fichier PYD est une bibliothèque liée dynamiquement à utiliser sur le système d'exploitation Windows.

## Comment créer un fichier PYD ?

Un fichier PYD peut être créé en créant un module avec un nom par exemple exmaple.pyd. Ce module contiendra toutes les fonctionnalités sous la forme d'une ou plusieurs fonctions, par exemple PyMod_example(). Lorsque le programme inclut cette bibliothèque et l'appelle, cela peut être fait en important le module et la fonction PyMod_example() s'exécutera.

## Références ##

* [Créer des extensions Python en C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Python_(programming_language))

