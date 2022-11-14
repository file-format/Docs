---
date: 2022-01-06
keywords: vtt, .vtt, format de fichier vtt, format de fichier .vtt, extension .vtt, extension vtt
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Découvrez le fichier .vtt et les API qui peuvent créer et ouvrir des fichiers VTT."
title: Format de fichier VTT - Fichier de pistes de texte vidéo Web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Qu'est-ce qu'un fichier VTT ?

Un fichier VTT est un fichier texte contenant des informations permettant d'afficher des pistes de texte chronométrées (telles que des sous-titres ou des légendes) à l'aide du format Web Video Text Tracks (WebVTT). Les pistes de texte chronométrées incluent des informations telles que des sous-titres ou des légendes. Le but du fichier VTT est d'ajouter des superpositions de texte à un<video> . Le format est quelque peu similaire aux fichiers SRT. Les fichiers texte basés sur WebVTT sont encodés en UTF-8. Un fichier VTT contient des informations telles que des sous-titres, des descriptions, des légendes, des descriptions, des chapitres et des métadonnées. En tant que fichiers texte brut, les fichiers VTT peuvent être ouverts à l'aide d'éditeurs de texte tels que Microsoft Notepad, Apple TextEdit et Notepad ++.

## Format de fichier VTT - Plus d'informations

Les fichiers VTT utilisent le format de fichier WebVTT pour enregistrer les informations de pistes de texte séquentielles. Chaque piste de texte chronométrée se compose d'une seule ligne ou de plusieurs lignes, également appelées "cue", comme illustré dans l'exemple suivant.

### Exemple de fichier VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Structure des fichiers VTT

Voici les exigences de structure d'un fichier VTT.

* Une marque d'ordre d'octet facultative (BOM).
* La chaîne "WEBVTT".
* Un en-tête de texte facultatif à droite de WEBVTT.
* Une ligne vide, qui équivaut à deux retours à la ligne consécutifs.
* Zéro ou plusieurs indices ou commentaires.
* Zéro ou plusieurs lignes vides.

## Références

* [VTT - Écoles W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

