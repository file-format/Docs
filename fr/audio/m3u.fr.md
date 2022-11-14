---
date: 2019-12-13
keywords: m3u, format de fichier m3u, extension .m3u, liste de lecture multimédia m3u, format de liste de lecture m3u
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier M3U et les API qui peuvent créer et ouvrir des fichiers M3U."
title: Format de fichier M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Qu'est-ce qu'un fichier M3U ? ##

M3U (URL MP3) est un fichier de liste de lecture audio stocké avec l'extension .m3u. M3U n'est pas un fichier audio réel, il pointe simplement vers des fichiers audio et parfois vidéo. M3U a été développé pour être utilisé avec le logiciel Winplay3 de Fraunhofer. Il est également pris en charge par divers lecteurs multimédias et logiciels.

## Format de fichier M3U

Il n'y a pas de spécification officielle pour le format de fichier M3U, c'est une norme de facto. M3U est un fichier texte brut qui utilise l'extension .m3u si le texte est encodé avec l'encodage non Unicode par défaut du système local ou avec l'extension .m3u8 si le texte est encodé en UTF-8. Chaque entrée du fichier M3U peut être l'une des suivantes :

- Chemin absolu vers le fichier
- Chemin du fichier relatif au fichier M3U.
- URL

### M3U étendu ###

Dans le M3U étendu, des directives supplémentaires sont introduites qui commencent par "#" et se terminent par deux-points (:) si elles ont des paramètres. Vous trouverez ci-dessous une liste de directives pour le M3U étendu.

- **#EXTM3U** - Il s'agit de l'en-tête de fichier indiquant Extended M3U et doit être la première ligne du fichier.
- **#EXTENC :** - Encodage de texte. Ce doit être la 2ème ligne du fichier.
- **#EXTINF :** - Utilisé pour les informations sur la piste et d'autres propriétés supplémentaires.
- **#PLAYLIST :** - Le titre de la playlist
- **#EXTGRP :** - Début du regroupement des noms
- **#EXTALB :** - Informations sur l'album
- **#EXTART :** - Artiste de l'album
- **#EXTGENRE** - Genre d'album
- **#EXTM3A** - Liste de lecture de fichier unique pour les pistes ou les chapitres de l'album.
- **#EXTBYT :** - Taille du fichier en octets.
- **#EXTBIN :** - Les données binaires suivent.
- **#EXTIMG :** - Logo, couverture ou autres images.

### HLS M3U ###

HLS (HTTP Live Streaming) a été créé par Apple pour diffuser de l'audio et de la radio sur des appareils iOS. Il est basé sur le M3U étendu encodé en UTF-8. Il a été normalisé en tant que RFC 8216 en 2017 par l'IETF. Les balises de la liste de lecture HLS commencent par "#EXT-X-". Vous trouverez ci-dessous une liste de balises pour HLS

- **EXT-X-VERSION** - Indique la version de compatibilité du fichier en fonction du support et de son serveur.
- **#EXT-X-START :** - Indique le point de départ préféré pour la liste de lecture.
- **#EXT-X-PLAYLIST-TYPE :** - Fournit le type de liste de lecture (ÉVÉNEMENT ou VOD).
- **#EXT-X-TARGETDURATION :** - Il spécifie la durée maximale du segment.
- **#EXT-X-MEDIA-SEQUENCE :** - Indique le numéro de séquence du média.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Indique que tous les échantillons de média sont indépendants et peuvent être décodés sans autres segments.
- **#EXT-X-MEDIA :** - Il est utilisé pour relier les listes de lecture multimédia qui contiennent des rendus alternatifs du même contenu.
- **#EXT-X-STREAM-INF :** - Il spécifie un flux de variante qui fait partie des rendus.
- **#EXT-X-BYTERANGE :** - Indique que le segment de média est une sous-gamme de la ressource identifiée par son URI.
- **#EXT-X-DISCONTINUITY** - Indique une discontinuité entre les segments média précédents et suivants.
- **#EXT-X-DISCONTINUITY-SEQUENCE :** - Permet la synchronisation entre différents rendus du même Variant Stream ou de différents Variant Streams.
- **#EXT-X-KEY :** - Spécifie comment décrypter les segments de média.
- **#EXT-X-MAP :** - Spécifie comment obtenir la section d'initialisation du support. Il est nécessaire d'analyser les segments de média applicables.
- **#EXT-X-PROGRAM-DATE-TIME :** - Il associe le premier échantillon du segment média à une date et/ou une heure absolue.
- **#EXT-X-DATERANGE:** - Il associe une Data Range.
- **#EXT-XI-FRAMES-ONLY** - Indique que chaque segment multimédia de la liste de lecture décrit une seule image I.
- **EXT-XI-FRAME-STREAM-INF** - Indique que le fichier de liste de lecture contient des images I de présentation multimédia.
- **#EXT-X-SESSION-DATA :** - Il permet aux données de session arbitraires d'être
transporté dans une liste de lecture principale.
- **#EXT-X-SESSION-KEY :** - Permet les clés de cryptage. Le client peut précharger ces clés sans lire la liste de lecture au préalable.
- **#EXT-X-ENDLIST** - Cela indique qu'aucun autre segment de média ne sera ajouté au fichier.

Voici la liste des types de médias Internet utilisés par M3U :

- **application/vnd.apple.mpegurl** : c'est le seul type de média enregistré (enregistré en 2009) pour M3U qui est utilisé pour faire référence aux listes de lecture dans les applications HLS.
- Les types de média Internet suivants sont utilisés par des applications non-HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Exemple M3U ##

Ceci est un exemple du fichier M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Références ##

- [M3U - Wikipédia](https://en.wikipedia.org/wiki/M3U)
- [Diffusion HTTP en direct] (https://tools.ietf.org/html/rfc8216)

