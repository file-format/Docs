---
date: 2019-10-11
keywords: vob, .vob, format de fichier vob, format de fichier .vob, extension .vob, extension vob, format vidéo vob, fichiers dvd vob
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier VOB et les API qui peuvent créer et ouvrir des fichiers VOB."
title: Format de fichier VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Qu'est-ce qu'un fichier VOB ? ##

Les fichiers VOB sont généralement stockés dans le répertoire VIDEO_TS sur un DVD avec une extension .vob. Les fichiers VOB contiennent des données vidéo et audio ainsi que d'autres données telles que des menus et des sous-titres. VOB est basé sur le format de flux de programme MPEG-2 mais il a des limitations et des spécifications supplémentaires dans les flux privés. Les fichiers VOB sont un sous-ensemble strict de flux de programmes MPEG. Tous les fichiers VOB sont donc des flux de programmes MPEG, mais tous les flux de programmes MPEG ne sont pas conformes à VOB.

## Structure du DVD vidéo ##

Lorsqu'un DVD est ouvert sur un ordinateur, VIDEO_TS est le répertoire de niveau supérieur avec AUDIO_TS. AUDIO_TS est vide et n'est pas utilisé. Dans le répertoire VIDEO_TS, il y a des fichiers VOB, BUP et IFO. Les fichiers VOB contiennent le contenu MPEG. Ceux-ci sont divisés en morceaux de 1 Go ou moins afin qu'ils soient compatibles avec tous les systèmes d'exploitation. Les fichiers IFO contiennent des informations concernant les menus et la structure des titres. Les fichiers BUK sont des fichiers de sauvegarde des fichiers IFO portant le même nom. Ces fichiers sont destinés à être conservés physiquement dans une zone séparée afin qu'au cas où le fichier IFO serait endommagé en raison de dommages physiques au DVD, le fichier BUK puisse fournir les mêmes informations.

### Disposition physique ###

- Tous les fichiers sur le disque doivent être contigus.
- Les fichiers associés doivent être côte à côte (VOB, IFO, BUP).
- Les fichiers numérotés doivent être dans l'ordre croissant.

## Protection contre la copie ##

De nombreux DVD vidéo sont cryptés et empêchent la copie des données du DVD. Des clés d'authentification et de déchiffrement sont nécessaires pour lire les fichiers situés dans la zone d'entrée inaccessible du DVD. Ces clés sont utilisées par le logiciel de décryptage CSS présent dans le lecteur DVD ou le lecteur logiciel. Sans les clés, les fichiers vidéo ne peuvent pas être lus car les clés seront demandées lors de l'ouverture des fichiers.

## Références ##

- [VOB - Wikipédia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

