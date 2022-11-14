---
date: 2019-10-11
keywords: f4v, .f4v, format de fichier f4v, format de fichier .f4v, extension .f4v, extension f4v, format vidéo f4v, comment ouvrir les fichiers f4v, que sont les fichiers f4v
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "En savoir plus sur le format de fichier F4V et les API qui peuvent créer et ouvrir des fichiers F4V"
title: Format de fichier F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Qu'est-ce qu'un fichier F4V ? ##

F4V (Flash MP4 Video File) est un fichier vidéo enregistré avec l'extension .f4v. Il est basé sur le format de fichier multimédia de base ISO (MPEG-4 Part 12). Il est très similaire à [MP4](/fr/video/mp4/), c'est pourquoi il est également appelé de manière informelle Flash MP4. [FLV](/fr/video/flv/) présentait des limitations lors de la diffusion de contenu H.264/ACC, ce qui a conduit Adobe Systems à créer le nouveau format F4V. Flash Player peut lire les fichiers F4V depuis la sortie de Flash Player 9 Update 3.

## Structure des fichiers F4V ##

Le format de fichier F4V est basé sur le format de fichier multimédia de base ISO (MPEG-4 Part 12) et est très similaire au format MP4. Pour les détails concernant la structure, veuillez consulter la page [MP4](/fr/video/mp4/). La principale différence entre F4V et MP4 réside dans les formats de métadonnées que F4V peut stocker. Vous trouverez ci-dessous la liste des formats de métadonnées pris en charge par le format F4V.

- **Boîte de balises** : quatre boîtes de balises supplémentaires facultatives (auth, titre, dscp, cprt) dans la boîte de film (moov).
- **Boîte de métadonnées XMP** : cette boîte vient juste après la boîte Film (moov). Avec cela, le fichier peut communiquer des métadonnées XMP à un film SWF via ActionScript.
- **ilst box** : cette boîte apparaît à l'intérieur de la boîte Meta (méta) et peut contenir un certain nombre de balises de métadonnées. Les types de données pris en charge sont indiqués ci-dessous.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Boîte de métadonnées de la piste de texte** : les échantillons de texte (texte ou tx3g) dans la boîte de données multimédia (mdat). Il peut contenir les boîtes de métadonnées suivantes.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Références ##

- [Vidéo Flash - Wikipédia](https://en.wikipedia.org/wiki/Flash_Video)

