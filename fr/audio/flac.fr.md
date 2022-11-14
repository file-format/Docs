---
date: 2019-12-13
keywords: flac, format de fichier flac, extension .flac, fichier flac, flac vs mp3
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier FLAC et les API qui peuvent créer et ouvrir des fichiers FLAC."
title: Format de fichier FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Qu'est-ce qu'un fichier FLAC ?

FLAC (Free Lossless Audio Codec) est un format de codage audio de compression sans perte développé par la Fondation Xiph.Org. FLAC est un format ouvert libre de droits enregistré avec l'extension .flac. L'audio numérique compressé à l'aide de l'algorithme FLAC est généralement réduit de 50 à 70 % en taille. Les fichiers FLAC peuvent être décompressés en une copie identique des fichiers audio originaux.

## Format de fichier FLAC

Ceci est un aperçu du flux binaire FLAC.

- **marqueur fLaC** : ce marqueur est ajouté au début du flux. Il est suivi d'un ou plusieurs blocs de métadonnées.
- **Blocs de métadonnées** : 128 types de blocs de métadonnées sont pris en charge par FLAC ; actuellement, les éléments suivants sont définis.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME** : les données audio sont composées d'une ou plusieurs trames audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Bref historique du format de fichier FLAC

Josh Coalson a commencé le développement de FLAC en 2000. La première version de FLAC a été publiée le 20 juillet 2001. FLAC a été incorporé sous le drapeau Xiph.Org le 20 janvier 2003. Le développement de FLAC a été déplacé vers le référentiel git Xiph.Org avec la sortie de la version 1.3.0 le 26 mars 2013.

## Composition du projet FLAC

Le projet FLAC comprend les éléments suivants :

- Formats de flux.
- Format de conteneur simple pour le flux (FLAC).
- libFLAC : une bibliothèque d'encodeurs, de décodeurs et d'interface de métadonnées de référence.
- libFLAC++ : un wrapper orienté objet pour libFLAC.
- flac : Un programme en ligne de commande pour encoder et décoder les flux FLAC.
- metaflac : Un éditeur de métadonnées en ligne de commande pour FLAC.
- Plugins d'entrée pour les lecteurs de musique comme Winamp, XMMX, etc.
- Format de conteneur Ogg (Ogg FLAC).

## Conception FLAC

Selon la densité et l'amplitude de la musique, la taille du fichier compressé peut être inférieure de 80 % à celle du fichier d'origine.

### Encodeur source ###

- Il ne prend en charge que les échantillons entiers et non en virgule flottante. Il peut gérer une résolution binaire PCM de 4 à 32 bits par échantillon et une fréquence d'échantillonnage de 1 Hz à 65 535 Hz. L'encodage FLAC est limité à 24 bits par échantillon.
- Les canaux peuvent être regroupés pour tirer parti des corrélations intercanaux afin d'augmenter la compression.
- Les sommes de contrôle CRC sont utilisées pour identifier les trames corrompues.
- Pour la conversion d'échantillons audio, FLAC utilise la prédiction linéaire.

### Métadonnées ###

- FLAC prend en charge ReplayGain (utilisé pour percevoir et normaliser le volume de l'audio).
- FLAC utilise le même système utilisé dans les commentaires Vorbis pour le marquage.
- libFLAC est utilisé par la plupart des applications FLAC pour l'encodage/décodage.
- L'API libFLAC est organisée en flux, flux recherchables et fichiers pour augmenter l'abstraction du flux binaire FLAC de base.

### Compression ###

libFLAC utilise des niveaux de compression de 0 à 8 où 0 est le niveau de compression le plus rapide et 8 est le niveau de compression le plus lent. Les fichiers compressés sont toujours sans perte bien que le compromis soit entre la vitesse et la taille.

## FLAC contre MP3
Le MP3 est un format de compression avec perte, ce qui signifie qu'il peut couper une partie de l'audio pour réduire sa taille après l'application de la compression. Alors que FLAC est un format de fichier sans perte, ce qui signifie que vous pouvez entendre l'audio dans sa forme la plus pure. Auparavant, les formats de fichiers sans perte étaient CDA ou WAV, qui n'étaient pas aussi économes en espace que FLAC. Le tableau suivant montrera la comparaison entre ces deux formats pour certains termes importants :

|Terme|FLAC|MP3|
---|---|---|
|**Qualité des données**|Aucune perte de données audio| Certaines données peuvent être perdues lors de la compression des données audio |
|**Taille**|Taille de fichier plus grande par rapport aux formats avec perte. Donc besoin d'une plus grande capacité de stockage | Taille de fichier plus petite, adaptée à la lecture sur des appareils audio compacts avec peu d'espace de stockage |
|**Configuration matérielle requise**| Besoin d'un équipement audio de haute qualité et d'une énorme capacité de stockage | D'énormes bibliothèques audio peuvent être enregistrées dans un espace de stockage plus petit. Convient aux appareils portables, tels que les lecteurs audio ou les téléphones mobiles |
|**Distribution sur Internet**|Ne peut pas être distribué facilement sur Internet en raison de la taille massive des fichiers |La taille compacte des fichiers facilite la distribution sur Internet|
|**Compatibilité**|Le codec d'écoute de musique et d'audio le plus populaire qui est à peu près compatible avec tous les appareils de la planèteCompatible avec les ordinateurs de nouvelle génération, les téléphones, les récepteurs AV, les lecteurs Blu-ray, les appareils de streaming comme Roku ou Fire TV|

## Références ##

- [FLAC - Wikipédia](https://en.wikipedia.org/wiki/FLAC)

