---
date: 2021-03-21
keywords: alac, format de fichier alac, extension .alac
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Découvrez le format de fichier ALAC et les API qui peuvent créer et ouvrir des fichiers ALAC."
title: ALAC - Format de fichier Apple Lossless Audio Codec
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Qu'est-ce qu'un fichier ALAC ?

Le format de fichier ALAC est Apple Lossless Audio Codec (ALAC) qui utilise le conteneur QuickTime compatible MPEG-4. Il a été introduit en 2004 en tant que format de fichier propriétaire, jusqu'en 2011, date à laquelle Apple l'a rendu disponible en open source et sans redevance. Le format est similaire au [FLAC](/fr/audio/flac/) (Free Lossless Audio Codec) mais offre plus de compression comparativement. Il offre une meilleure alternative sonore à [AAC](/fr/audio/aac/) ou [MP3](/fr/audio/mp3/). Les fichiers audio encodés avec le codec ALAC peuvent être ouverts à l'aide d'Apple QuickTime, d'Apple iTunes et de Micrsoft Windows Media Player avec le codec K-Lite.

## Format de fichier ALAC

Les fichiers basés sur le codec ALAC sont des fichiers binaires disponibles en [open source sur GitHub](https://github.com/macosforge/alac) pour la référence du développeur. Il contient les sources de l'encodeur et du décodeur ALAC. Apple a également fourni un utilitaire de ligne de commande, appelé "alacconvert", pour lire et écrire les données audio vers/depuis les fichiers Core Audio Format (CAF) et [WAVE](/fr/audio/wav/). Voici quelques points clés concernant le format de fichier ALAC.

1. "Profondeurs de bits" - 16, 20, 24 et 32 bits.
1. `Sample Rate` - Tout taux d'échantillonnage entier arbitraire de 1 à 384 000 Hz. Des fréquences théoriques allant jusqu'à 4 294 967 295 (2 ^ 32 - 1) Hz pourraient être prises en charge.
1. "Taille de paquet" - La taille de paquet par défaut est de 4096 trames d'échantillons audio par paquet. D'autres tailles de paquets sont certainement possibles. Cependant, il n'est pas garanti que les tailles de paquet autres que celles par défaut fonctionnent correctement sur tous les périphériques matériels prenant en charge Apple Lossless. Les paquets supérieurs à 16 384 trames d'échantillonnage ne sont pas pris en charge.
1. "Canaux pris en charge" - Il prend en charge un à huit canaux. Chaque canal a l'ordre d'informations suivant.

|Num Chan| Commande|
|---|---|
|1 |mono|
|2 |stéréo (Gauche, Droite)|
|3 |MPEG 3.0 B (Centre, Gauche, Droite)|
|4 |MPEG 4.0 B (Centre, Gauche, Droite, Centre Surround)|
|5 |MPEG 5.0 D (Centre, Gauche, Droite, Surround gauche, Surround droite)|
|6 |MPEG 5.1 D (Centre, Gauche, Droite, Surround gauche, Surround droite, Effets basse fréquence)|
|7 |Apple AAC 6.1 (Centre, Gauche, Droite, Surround gauche, Surround droit, Surround central, Effets basse fréquence)|
|8 |MPEG 7.1 B (Centre, Centre gauche, Centre droit, Gauche, Droite, Surround gauche, Surround droit, Effets basse fréquence)|

## Références

* [ALAC - Wikipédia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Codec audio sans perte Apple](https://macosforge.github.io/alac/)
* [macosforge - alac sur GitHub](https://github.com/macosforge/alac)

