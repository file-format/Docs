---
date: 2019-10-11
keywords: flv, .flv, format de fichier flv, format de fichier .flv, extension .flv, extension flv, format vidéo flv
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier FLV et les API qui peuvent créer et ouvrir des fichiers FLV."
title: Format de fichier FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Qu'est-ce qu'un fichier FLV ? ##

FLV (Flash Video) est un format de fichier conteneur avec l'extension .flv. FLV est utilisé pour diffuser du contenu audio/vidéo sur Internet à l'aide d'Adobe Flash Player ou d'Adobe Air. Les données des fichiers FLV sont encodées de la même manière que les fichiers SWF. La prise en charge directe a été ajoutée à Flash Player 7 en 2003. Les systèmes Adobe ont créé F4V en 2007 en raison des restrictions de FLV.

### Encodage ###

Les fichiers FLV contiennent des flux binaires vidéo de Sorenson Spark qui sont une variante propriétaire de la norme vidéo H.263. Il s'agit du format de compression requis pour Flash Player 6 et 7. La version 8 de Flash Player prend en charge les flux binaires vidéo On2 TrueMotion VP6. Il s'agit du format de compression recommandé pour Flash Player 8 et supérieur. FLV prend en charge l'audio au format MP3, le codec Nellymoser Asao et le codec open source Speex. Il prend également en charge l'audio non compressé ou l'audio au format ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile et AAC-LC) sont pris en charge par les versions récentes de Flash Player 9.

## Structure ##

Les fichiers FLV se composent d'en-tête et de paquets. Un fichier FLV commence par l'en-tête. L'en-tête contient les champs suivants.

- **Signature** : sa valeur est FLV
- **Version** : sa valeur par défaut est 1. Seul 0x01 est valide.
- **Drapeaux** : 0x04 est utilisé pour l'audio et 0x01 est utilisé pour la vidéo, donc 0x05 est utilisé à la fois pour l'audio et la vidéo.
- **Taille de l'en-tête** : la valeur par défaut est 9. Elle est utilisée pour ignorer un en-tête développé plus récent.

Après l'en-tête viennent les paquets. Le fichier FLV est divisé en plusieurs paquets appelés balises FLV qui ont des en-têtes de 15 octets. Les paquets contiennent les métadonnées pour l'audio, la vidéo, les scripts, les informations de chiffrement et la charge utile. Les paquets FLV ont les champs suivants.

- **Réservé** : Il est réservé au FMS et doit être 0.
- **Filtre** : Indique si les paquets sont filtrés ou non.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Type de paquet** : définit le type de contenu du paquet.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Taille des données** : indique la longueur du message.
- **Timestamp Lower** : cela stocke l'horodatage en millisecondes auquel les données de balise s'appliquent. Il est défini sur NULL pour le premier paquet.
- **Timestamp Upper** : Extension pour créer une valeur uint32_be.
- **ID de flux** : défini sur NULL pour le premier flux.
- **Données de charge utile** : il s'agit des données basées sur le type de paquet.

## Références ##

- [Vidéo Flash - Wikipédia](https://en.wikipedia.org/wiki/Flash_Video)

