---
date: 2022-05-09
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fichier PYI - Définition de l'interface Python
linktitle: PYI
description: "Découvrez le format de fichier PYI et les API qui peuvent créer et ouvrir des fichiers PYI."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Qu'est-ce qu'un fichier PYI ?

Un fichier PYI est un fichier de définition d'interface Python qui contient une référence de stub de code pour l'implémentation de l'interface. Chaque module Python est représenté comme un stub .pyi qui est un fichier Python normal mais avec des méthodes vides. La syntaxe des fichiers PYI est la même que celle d'un module Python normal. La mise en œuvre des méthodes vides est laissée à l'utilisateur final pour atteindre l'objectif spécifique pour lequel le module est écrit. C'est là que les fichiers PYI sont différents des fichiers [PY](/fr/programming/py/) qui contiennent l'implémentation complète du programme. Les fichiers PYI peuvent être ouverts avec des éditeurs de texte tels que Notepad, Notepad++, Microsoft Visual Studio Code et JetBrains PyCharm.

## Format de fichier PYI

Les fichiers PYI sont enregistrés sous forme de fichiers texte brut pouvant être ouverts avec n'importe quel éditeur de texte. Python est un langage interpréteur qui effectue une vérification de type lorsque le code est exécuté. Dans ce cas, les fichiers PYI sont avantageux dans la mesure où les développeurs peuvent définir et vérifier manuellement les types d'un module lors de l'écriture de l'application.

## Références ##

* [Interfaces - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [Interprètes PYM](https://github.com/interpreters/pym)

