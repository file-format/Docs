---
date: 2019-10-11
keywords: rm, .rm, format de fichier rm, format de fichier .rm, extension .rm, format de fichier RealMedia
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier RM et les API qui peuvent créer et ouvrir des fichiers RM."
title: Format de fichier RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Qu'est-ce qu'un fichier RM ? ##

RealMedia est un format de conteneur multimédia propriétaire développé par RealNetworks qui utilise l'extension .rm. Il est utilisé avec la combinaison de [RealAudio (RA)](/fr/audio/ra/) et [RealVideo(RV)](/fr/video/rv/) pour le streaming sur Internet. Ces flux sont à débit binaire constant. Pour le débit binaire variable, RealNetworks a développé le format RealMedia Variable Bitrate (RMVB). RealMedia convient à la diffusion de contenu sur Internet et peut être utilisé par exemple pour diffuser la télévision en direct.

## Structure du fichier RealMedia ##

Un fichier RealMedia se compose d'une série de morceaux, chacun ayant la structure suivante :

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Voici les types de morceaux présents dans le fichier RealMedia :

- **En-tête de fichier RealMedia (.RMF)** : il doit s'agir du premier bloc du fichier RealMedia. Un seul bloc RMF est présent dans un fichier. Il contient des informations sur le nombre d'en-têtes.
- **En-tête des propriétés du fichier (PROP)** : contient des informations sur les propriétés générales du fichier RealMedia. Il n'y a qu'un seul bloc de ce type dans chaque fichier RealMedia.
- **En-tête des propriétés du média (MDPR)** : ce bloc contient des informations sur les propriétés du flux. Il contient des informations sur le type de flux et le codec utilisé. Il existe un bloc MDPR pour chaque flux dans le fichier.
- **En-tête de description de contenu (CONT)** : ce bloc contient des informations textuelles telles que le titre ou l'auteur du contenu du fichier RealMedia. Ce bloc est à titre informatif uniquement.
- **En-tête de données (DATA)** : ce bloc contient un groupe de paquets de données.
- **En-tête d'index (INDX)** : ce bloc vient après tous les blocs de données et contient des entrées d'index. Un fichier peut avoir plusieurs blocs INDX.

## Formats audio et vidéo pris en charge ##

### Formats audio ###

- lpcJ : RealAudio 1.0 (VSELP)
- 28_8 : RealAudio 2.0 (LD-CELP
- dnet : AC3
- sipr : Sipro
- cuisinier : Cuisinier
- atrc : ATRAC3
- ralf : format sans perte RealAudio
- raac : LC-AAC
- racp : HE-AAC

### Format vidéo ###

- CLV1 : ClearVideo
- RV10 : H.263
- RV13 : H.263
- RV20 : H.263+, RV20
- RV30 : précurseur H.264
- RV40 : précurseur H.264, RV40
- RVTR : H.263+ (RV20)

## Références ##

- [RealMedia - Wikipédia](https://en.wikipedia.org/wiki/RealMedia)

