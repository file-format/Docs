---
date: 2019-10-11
keywords: MP4, fichier, extension, format, format vidéo, MPEG-4
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier MP4 et les API qui peuvent créer et ouvrir des fichiers MP4."
title: Format de fichier MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Qu'est-ce qu'un fichier MP4 ? ##

MP4 (abréviation de MPEG-4 Part 14) est un format de fichier basé sur ISO/IEC 14496-12:2004 qui est basé sur le format de fichier QuickTime mais spécifie formellement la prise en charge des descripteurs d'objets initiaux (IOD) et d'autres fonctionnalités MPEG. Il est principalement utilisé pour stocker de la vidéo et de l'audio, mais peut également être utilisé pour stocker des sous-titres et des images fixes. Les fichiers MP4 sont stockés avec l'extension .mp4. MP4 est une norme internationale de codage audiovisuel. Semblable à la plupart des formats de conteneurs modernes, MP4 prend en charge la diffusion en continu sur Internet. En raison de la compression élevée utilisée dans MP4, les fichiers résultants sont de plus petite taille avec presque toute la qualité d'origine conservée.

## Bref historique ##

La spécification MP4 a été développée par le Moving Picture Experts Group (MPEG) et était basée sur le format QuickTime [MOV](/fr/video/mov/) qui a été publié en 2001. La première version (ISO/IEC 14496-1:2001) de MP4 était une révision de la spécification MPEG-4 Part 1: Systems publiée en 1999. Le format de fichier MP4 a été généralisé au format de fichier multimédia de base ISO ISO / CEI 14496-12: 2004 qui définissait la structure générale des fichiers multimédias temporels. En conséquence, il est utilisé comme base pour d'autres formats de fichiers.

## Structure des fichiers MP4 ##

MP4 est un fichier conteneur extensible, ce qui signifie qu'il ne définit pas de structure stricte et permet une structure et une hiérarchie personnalisées pour chaque type de média. Les données du fichier MP4 sont divisées en deux sections, la première contenant les données relatives aux médias et la seconde contenant les métadonnées. Les données multimédias contiennent de l'audio ou de la vidéo et les métadonnées indiquent des drapeaux pour un accès aléatoire, des horodatages, etc.
Les structures dans MP4 sont généralement appelées atomes ou boîtes. La taille minimale d'un atome est de 8 octets (les 4 premiers octets spécifient la taille et les 4 octets suivants spécifient le type). Voici une liste des atomes de niveau racine contenus dans les fichiers MP :

- **ftyp** : Contient le type de fichier, sa description et les structures de données communes utilisées.
- **pdin** : Contient des informations de chargement/téléchargement vidéo progressif.
- **moov** : Conteneur pour toutes les métadonnées du film.
- **moof** : Conteneur contenant des fragments vidéo.
- **mfra** : le conteneur avec un accès aléatoire au fragment vidéo
- **mdat** : Conteneur de données pour les médias.
- **stts** : tableau échantillon-temps.
- **stsc** : table sample-to-chunk.
- **stsz** : tailles d'échantillons (cadrage)
- **meta** : le conteneur contenant les informations de métadonnées.

Voici une liste d'atomes de second niveau utilisés dans MP4 :

- **mvhd** : Contient les informations d'en-tête de la vidéo avec tous les détails de la vidéo.
- **trak** : Conteneur avec la piste individuelle.
- **udta** : le conteneur contenant les informations sur l'utilisateur et la piste.
- **iods** : descripteur de fichier MP4

## Références ##

- [MP4 - Wikipédia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

