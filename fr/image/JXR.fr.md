---
date: 2020-08-12
keywords: jxr, .jxr, format de fichier jxr, comment ouvrir les fichiers jxr, extension .jxr, extension jxr
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier JXR
linktitle: JXR
description: "Découvrez le format de fichier JXR et les API qui peuvent créer et ouvrir des fichiers JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Qu'est-ce qu'un fichier JXR ? ##

JPEG XR (gamme étendue JPEG) est un format de fichier pour les images photographiques à tons continus. Il s'agit d'une norme de compression d'images fixes basée sur HD Photo développée par Microsoft. Il prend en charge la compression avec et sans perte.

## Bref historique ##

Windows Media Photo a été annoncé pour la première fois par Microsoft lors de WinHEC 2006. Il a été renommé HD Photo en novembre 2006. JPEG XR a été approuvé en tant que norme internationale ISO/IEC 29199-2 le 19 juin 2009. L'UIT-T et l'ISO/IEC ont publié une motion spécification de format (ITU-T T.833 | ISO/IEC 29199-3), un ensemble de tests de conformité (ITU-T T.834 | ISO/IEC 29199-4) et un logiciel de référence (ITU-T T.835 | ISO /IEC 29199-5) pour JPEG XR après l'achèvement de la spécification de codage d'image en 2010. Un rapport technique décrivant l'architecture de flux de travail pour JPEG XR a été publié en 2011.

## Conception JPEG XR ##

Par rapport à JPEG, JPEG XR offre plusieurs améliorations dont :

- **Meilleure compression** : JPEG XR offre des taux de compression plus élevés.
- **Compression sans perte** : JPEG XR prend en charge la compression sans perte.
- **Structure de tuiles** : l'image JPEG XR peut être segmentée en régions de tuiles où chaque région peut être décodée séparément.
- **Plus de précision des couleurs** : JPEG XR inclut la conversion interne vers l'espace colorimétrique YCoCg pour prendre en charge les images utilisant l'espace colorimétrique RVB. JPEG XR prend également en charge un modèle de couleur CMJN entier de 16 bits par composant (64 bits par pixel). JPEG XR prend en charge le format de couleur à virgule flottante à exposant partagé RGBE pour les images HDR. JPEG XR prend également en charge les encodages de couleurs en niveaux de gris et multicanaux.
- **Transparency Map** : JPEG XR prend en charge le canal alpha pour la transparence.
- **Modification d'image de domaine compressé** : les images JPEG XR peuvent être converties en codage avec perte, réduites en résolution, recadrées, retournées, pivotées et la structure des tuiles peut être modifiée sans décodage complet du fichier.
- ** Prise en charge des métadonnées ** : le fichier image JPEG XR peut contenir un profil de couleur ICC pour une représentation cohérente des couleurs sur plusieurs appareils. Le format prend également en charge les formats de métadonnées Exif et XMP.

## Format de conteneur ##

Les données d'image JPEG XR peuvent être stockées dans un format de conteneur de type TIFF à l'aide d'un tableau de balises IFT (Image File Directory). Un fichier JXR contient les éléments suivants dans les balises IFD :

- Données d'image : Il s'agit de données d'image autonomes contiguës.
- Optional alpha channel data: If this is present, the image data can be compressed separately enabling the support of applications that do not support transparency.

- Métadonnées
- Métadonnées XMP facultatives
- Métadonnées Exif facultatives

Comme il est basé sur le format TIFF, il hérite de toutes les limitations du format TIFF comme la limite de taille de fichier de 4 Go.

## Références ##

- [JPEG XR - Wikipédia](https://en.wikipedia.org/wiki/JPEG_XR)

