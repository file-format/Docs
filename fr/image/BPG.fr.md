---
date: 2020-08-12
keywords: bpg, .bpg, format de fichier bpg, comment ouvrir des fichiers bpg, extension .bpg, extension bpg
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier BPG
linktitle: BPG
description: "Découvrez le format de fichier BPG et les API qui peuvent créer et ouvrir des fichiers BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Qu'est-ce qu'un fichier BPG ? ##

BPG (Better Portable Graphics) est un format de fichier créé par Fabrice Bellard en 2014 pour les images numériques. Il a proposé BPG en remplacement de JPEG car BPG était plus efficace en termes de compression ou de taille. BPG utilise le codage intra-image de la norme de compression vidéo HEVC (High-Efficiency Video Coding).

BPG est conçu comme un format portable économe en mémoire pour fonctionner sur des appareils portables et IoT. Actuellement, les navigateurs Web ne prennent pas en charge le format BPG, mais les sites Web peuvent toujours fournir des images BPG en utilisant une bibliothèque JavaScript écrite par Bellard. BPG utilise le profil principal 4:4:4 16 images fixes du HEVC jusqu'à 14 bits par échantillon.

## Caractéristiques ##

Le format de conteneur BPG est un format d'image générique plutôt que le flux binaire brut utilisé dans HEVC. BPG prend en charge les formats de couleurs 4:4:4, 4:2:2 et 4:2:0. Le canal alpha est également pris en charge avec un canal supplémentaire codé séparément ou le quatrième canal de l'image CMJN. BPG prend en charge les métadonnées pour les profils Exif, ICC et XMP. BPG prend en charge YCbCr (ITU-R BT.601, BT.709 et BT.2020 (luminance non constante)), YCgCo, RVB, CMJN et l'espace colorimétrique en niveaux de gris. BGP prend également en charge l'animation et la compression de données HEVC avec et sans perte.

## Références ##

- [Meilleurs graphiques portables - Wikipedia] (https://en.wikipedia.org/wiki/Better_Portable_Graphics)

