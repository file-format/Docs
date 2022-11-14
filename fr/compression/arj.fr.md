---
date: 2019-12-09
keywords: arj, .arj, format de fichier arj, comment ouvrir les fichiers arj, extension .arj, extension arj
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier ARJ
linktitle: ARJ
description: "Découvrez le format de fichier ARJ et les API qui peuvent créer et ouvrir des fichiers ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Qu'est-ce qu'un fichier ARJ ? ##

ARJ (Archivé par Robert Jung) est un fichier d'archive compressé à haute efficacité développé par Robert K. Jung. ARJ a été développé pour DOS et les premières versions de Windows au début des années 1990. Les fichiers ARJ sont utiles pour sauvegarder ou partager un grand nombre de fichiers car vous n'avez pas à suivre tous ces fichiers et il n'y a qu'un seul fichier à gérer. L'extension .arj est utilisée pour les fichiers d'archive ARJ.

## Format de fichier ARJ ##

Un fichier ARJ contient deux types d'en-têtes :

- En-tête principal : Il y a un en-tête principal au début de l'archive.
- En-têtes locaux : Les en-têtes locaux sont présents avant chaque fichier.

|Décalage|Type|Compte|Description|
|---|---|---|---|
|0000h|mot|1|ID=0EA60h|
|0002h|mot|1|taille d'en-tête de base|
|0004h|octet|1|Taille de l'en-tête|
|0005h|byte|1|Numéro de version de l'archiveur|
|0006h|byte|1|Numéro de version minimum nécessaire|
|0007h|octet|1|OS hôte :</br> 0 - MS-DOS</br> 1 - PRIMO</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Système xx)</br> 5 - OS/2</br> 6 - POMME GS</br> 7 - ATARI ST</br> 8 - SUIVANT</br> 9 - VAX VMS|
|0008h|byte|1|Drapeaux internes, bitmap :</br> 0 - pas de mot de passe / mot de passe</br> 1 - réservé</br> 2 - le fichier continue sur le disque suivant</br> 3 - le champ de position de début de fichier est disponible</br> 4 - traduction du chemin ( "\" vers "/" )|
|0009h|octet|1|Méthode de compression :</br> 0 - stocké</br> 1 - le plus compressé</br> 2 - compressé</br> 3 - compressé plus rapidement</br> 4 - compressé le plus rapidement |
|000Ah|octet|1|Type de fichier :</br> 0 - binaire</br> 1 - Texte 7 bits</br> 2 - en-tête de commentaire</br> 3 - répertoire</br> 4 - étiquette de volume |
|000Bh|octet|1|réservé|
|000Ch|dword|1|Date/Heure du fichier d'origine au format MS-DOS|
|0010h|dword|1|Taille du fichier compressé|
|0014h|dword|1|Taille du fichier d'origine"|
|0018h|dword|1|CRC-32 du fichier d'origine|
|001Ah|word|1|Position de la spécification de fichier dans le nom de fichier|
|001Ch|mot|1|Attributs de fichier|
|001Eh|mot|1|Données hôte|
|?|dword|1|Position de départ du fichier étendu|
|????h|dword|1|CRC-32 de l'en-tête de base|
|????h|mot|1|Taille du premier en-tête étendu|
|????h+"SIZ"+2|dword|1|CRC-32 de l'en-tête étendu|
|????h+"SIZ"+6|octet|?|Fichier compressé|

## Références ##

- [ARJ - Wikipédia](https://en.wikipedia.org/wiki/ARJ)

