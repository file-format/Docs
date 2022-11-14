---
date: 2019-10-11
keywords: srt, .srt, format de fichier srt, format de fichier .srt, extension .srt, extension srt
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Découvrez le format de fichier SRT et les API qui peuvent créer et ouvrir des fichiers SRT."
title: Format de fichier SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Qu'est-ce qu'un fichier SRT ? ##

SRT (format de fichier SubRip) est un simple fichier de sous-titre enregistré au format de fichier SubRip avec l'extension .srt. Il contient un nombre séquentiel de sous-titres, des horodatages de début et de fin et un texte de sous-titre. Les fichiers SRT permettent d'ajouter des sous-titres au contenu vidéo après sa production.

## Structure du fichier SRT ##

Chaque sous-titre comporte quatre parties dans le fichier SRT.

1. Un compteur numérique indiquant le numéro ou la position du sous-titre.
1. Heure de début et de fin du sous-titre séparées par --> caractères
1. Texte du sous-titre sur une ou plusieurs lignes.
1. Une ligne vide indiquant la fin du sous-titre.

### Exemple de SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Pour spécifier l'heure, le format *heures:minutes:secondes,millisecondes (00:00:00,000)* est utilisé.

## Formatage des fichiers SRT ##

Le formatage des fichiers SRT est dérivé des balises HTML. Les balises de formatage du fichier SRT sont répertoriées ci-dessous.

| Effet | Balises |
| --- | --- |
|Gras|**\ <b>...\</b> ** ou {b}...{/b}|
|Italique|**\ <i>...\</i> ** ou **{i}...{/i}**|
|Souligné|**\ <u>...\</u> ** ou **{u}...{/u}**|
|Couleur de police|**\ <font color="white">...\</font> **|
|Line Position|**{\a3}** (indique que le texte doit commencer à apparaître sur la ligne 3)

## Logiciel SubRip ##

SubRip est un logiciel gratuit qui fonctionne sous Windows. Il extrait les sous-titres et leur minutage à partir de différents formats vidéo et enregistre les sous-titres au format SRT. SubRip utilise la reconnaissance optique des caractères pour extraire les sous-titres de la vidéo en direct, d'autres fichiers vidéo et de DVD.

## Références ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
