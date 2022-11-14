---
date: 2021-07-05
keywords: ssp, .ssp, format de fichier ssp, comment ouvrir les fichiers ssp, Scala Server Page
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Format de fichier des pages du serveur Scala
linktitle: SSP
description: "Découvrez ce qu'est un format de fichier SSP et les API qui peuvent créer et ouvrir des fichiers SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Qu'est-ce qu'un fichier SSP ?

Un fichier avec l'extension .ssp est une page Web créée avec du code Scala pour les expressions au lieu du HTML brut uniquement. Il agit comme un script côté serveur en utilisant la combinaison de HTML et Scala. Ces fichiers résident sur le serveur et sont utilisés pour créer des pages Web statiques à servir aux utilisateurs. Scala lui-même est un langage de programmation à usage général dont la syntaxe est familière aux utilisateurs qui ont travaillé avec Velocity, JSP ou Erb. Les fichiers SSP peuvent être analysés et évalués à l'aide de [Scalate](https://scalate.github.io/scalate/) qui est un moteur de modèle basé sur Scala pour générer du texte et du balisage.

## Format de fichier SSP - Plus d'informations

Les fichiers SSP sont enregistrés dans un fichier texte brut et peuvent être évalués à l'aide de Scalate. Un modèle Ssp se compose de texte brut qui est le plus souvent le document HTML. Il contient des balises Ssp intégrées qui obligent les moteurs de rendu à restituer dynamiquement différentes parties du document. Les balises commencent et se terminent par la séquence <% ... %> et ${ ... } et tout ce qui se trouve en dehors de celles-ci est considéré comme du texte littéral.

### Exemple de fournisseur de services partagés

L'exemple suivant montre le code SSP et sa sortie lorsqu'il est rendu par le moteur de rendu.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
La sortie est la suivante.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Références

- [Référence SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

