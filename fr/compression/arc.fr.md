---
date: 2019-12-09
keywords: arc, .arc, format de fichier arc, comment ouvrir des fichiers arc, extension .arc, extension arc
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier ARC
linktitle: ARC
description: "Découvrez le format de fichier ARC et les API qui peuvent créer et ouvrir des fichiers ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Qu'est-ce qu'un fichier ARC ?

ARC est un format de compression et d'archivage de données sans perte développé par System Enhancement Associates (SEA). Le format de fichier et l'application qui le crée s'appellent ARC. ARC était très populaire au début du BBS commuté car il combinait les fonctionnalités de compression et d'archivage de plusieurs fichiers dans le même fichier. ARC a ensuite été remplacé par [ZIP](/fr/compression/zip/) qui offrait de meilleurs taux de compression.

L'extension de fichier .arc est utilisée par plusieurs autres types de fichiers d'archive non liés, comme le format ARC utilisé par Internet Archive pour stocker plusieurs ressources Web, un format ARC différent utilisé par l'archiveur FreeArc, un format différent utilisé par Nintendo pour les ressources, etc. .

## Bref historique du format de fichier ARC

Le programme ARC a été écrit par Thom Henderson de System Enhancement Associates en 1985. Ce programme a regroupé les fichiers dans un seul fichier d'archive et les a également compressés. Les fichiers générés par le programme ARC utilisaient l'extension .arc. SEA a publié le code source d'ARC en 1986 et ARC a été porté sur Unix et Atari ST par Howard Chu en 1987.

Phil Katz a développé PKARC et PKXARC pour l'archivage et l'extraction de fichiers. Les fichiers fonctionnaient avec le format de fichier ARC et étaient beaucoup plus rapides. Contrairement à ARC, Katz a divisé les fonctions de compression et d'archivage entre deux fichiers différents, ce qui a réduit les besoins en mémoire pour les exécuter.

Après le procès entre SEA et Katz, SEA s'est retiré du marché du shareware et a développé ARC+Plus avec une interface utilisateur plein écran. Le format ARC n'est plus courant sur PC.

## Format de fichier ARC

Le fichier ARC se compose d'une séquence d'en-tête de fichier et de fichier suivi du marqueur de fin d'archive, comme indiqué ci-dessous.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### En-tête de fichier ARC ###

|Décalage|Étiquette|Type|Valeur|Description|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Méthode|
|02|ARCFNT|DS|12|nomfichier|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Taille compressée|
|13|ARCDAT|DW|0000|Date du fichier (MSDOS)|
|15|ARCTIM|DW|0000|Heure du fichier (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Taille non compressée|
|1D|ARCFIL|DS|ARCNSZ| |

### Méthodes de compression ###

L'octet de méthode de compression indique la méthode de compression utilisée. Voici les méthodes de compression utilisées pour le fichier ARC.

|Méthode|Nom|Description|
|---|---|---|
|0|Stocké|Aucune compression utilisée|
|1|Empaqueté|Codage de longueur courante répété (RLE)|
|2|Compressé|Codage de Huffman|
|3|Crunched|LZW avec tampon 4K, codes 12 bits|
|4|Crunched|Premier compactage, puis tampon LZW 4K avec 12 bits|
|5|Crunched|Packing, LZW, tampon 4K, longueur variable (9-12 bits)|
|6|Écrasé|LZW, tampon 8K, longueur variable (9-13 bits)|
|7|Écrasé|Emballage, puis tampon LZW 8K, 2-13 bits (PAK 1.0)|
|8|Distillation|Dynamic Huffman avec mémoire tampon 8K (PAK 2.0)|

## Références

- [ARC (format de fichier) - Wikipédia](https://en.wikipedia.org/wiki/ARC_(file_format))

