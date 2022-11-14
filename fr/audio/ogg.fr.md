---
date: 2019-12-13
keywords: ogg, format de fichier ogg, extension .ogg, format audio ogg
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier OGG et les API qui peuvent créer et ouvrir des fichiers OGG."
title: Fichier OGG - Fichier audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Qu'est-ce qu'un fichier OGG ?

OGG est un fichier audio compressé Ogg Vorbis enregistré avec l'extension .ogg. Les fichiers OGG sont utilisés pour stocker des données audio et peuvent également inclure des informations sur l'artiste et la piste, ainsi que des métadonnées. OGG est un format de conteneur gratuit et ouvert qui est géré par la Fondation Xiph.Org.

## Bref historique du format de fichier OGG

Le projet Ogg a commencé dans le cadre d'un projet plus vaste en 1993 et s'appelait Squish, mais en raison d'une marque existante, il a été renommé OggSquish. Il a été décrit comme une tentative de créer un format audio compressé flexible pour les applications audio modernes. La référence OGG a été séparée de Vorbis le 2 septembre 2000.

OGM a été créé en 2002 en raison du manque de support vidéo formel dans OGG. Cela a permis d'intégrer la vidéo du framework Microsoft DirectShow dans un wrapper basé sur OGG. En 2006, OGG était pris en charge par de nombreux moteurs de jeux vidéo et était couramment utilisé pour encoder du contenu gratuit. La Free Software Foundation a lancé une campagne le 15 mai 2007 pour accroître l'utilisation de Vorbis comme alternative supérieure au MP3. Au 30 juin 2009, OGG était le seul format de conteneur pris en charge par l'implémentation HTML5 de Firefox 3.5.

## Format de fichier OGG

Le format OGG se compose de blocs de données. Chaque bloc est appelé une page Ogg. Chaque page commence par "OggS" pour identifier le format Ogg. L'en-tête contient le numéro de série et le numéro de page qui identifie chaque page comme faisant partie d'une série. La page se compose des composants suivants.

- **En-tête de page**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| peu | Valeur | Descriptif |
| --- | --- | --- |
| 0 | 0x01 | Indique que le premier paquet de la page est la continuation du paquet précédent dans le train binaire logique. |
| 1 | 0x02 | Indique que cette page est la première du flux binaire logique. |
| 2 | 0x04 | Indique que cette page est la dernière du flux binaire logique. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Métadonnées** : VorbisComment est le mécanisme le plus largement pris en charge pour le stockage des métadonnées. Les autres mécanismes comprennent les suivants :
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Références ##

- [OGG - Wikipédia](https://en.wikipedia.org/wiki/Ogg)

