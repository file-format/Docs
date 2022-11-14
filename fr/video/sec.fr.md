---
date: 2022-03-25
keywords: sec, .sec, format de fichier sec, format de fichier .sec, extension .sec, extension sec
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Découvrez le format de fichier SEC et les API qui peuvent créer et ouvrir des fichiers SEC."
title: Format de fichier SEC - Fichier vidéo de sécurité Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Qu'est-ce qu'un fichier SEC ?

Un fichier SEC est un fichier vidéo créé avec le système de surveillance Samsung DVR. La vidéo est capturée à partir des caméras de surveillance et stockée sur disque au format SEC. La vidéo SEC enregistrée peut être lue avec le logiciel vidéo de Samsung qui peut gérer le flux vidéo de plusieurs caméras.

## Format de fichier SEC - Plus d'informations

Les fichiers SEC contiennent un flux h264/AVC à l'intérieur en utilisant un format de fichier propriétaire. L'en-tête d'un fichier SEC commence par le numéro de modèle du SRD-1670D. Les informations de date et d'heure sont conservées à la fin du fichier.

### Convertir le fichier SEC en AVI

Le fichier SEC peut être converti au format de fichier standard [AVI](/fr/video/avi/) à l'aide de FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Références ##

- [Fichiers Samsung et SEC] (https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

