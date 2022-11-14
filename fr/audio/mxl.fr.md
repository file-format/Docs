---
date: 2022-03-20
keywords: mxl, format de fichier Musepack, extension .mxl
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Découvrez le format de fichier MXL et les API qui peuvent créer et ouvrir des fichiers MXL."
title: Format de fichier MXL - Fichier MusicXML compressé
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Qu'est-ce qu'un fichier MXL ?

Un fichier MXL est la forme compressée du format de fichier MusicXML qui est un format standard ouvert pour l'échange de partitions numériques. Les fichiers MusicXML en texte brut sont volumineux et l'utilisation de tels fichiers comme format de distribution de feuilles a été affectée par la grande taille du fichier. Ce problème a été traité avec [MusicXML](https://www.musicxml.com/) 2.0 en introduisant le format de fichier MXL qui compresse suffisamment les fichiers pour réduire la taille du fichier de manière similaire à celle des fichiers MIDI d'origine. Le type de média recommandé pour les fichiers MXL est application/vnd.recordare.musicxml.

## Format de fichier MXL

Les fichiers MXL sont stockés sous forme de fichiers [XML](/fr/web/xml/) compressés [ZIP](/fr/compression/zip/) avec l'extension de fichier .mxl. Les fichiers MXL sont compressés avec l'algorithme DEFLATE comme spécifié dans la [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Structure des fichiers MXL

Chaque fichier MXL a un format XML basé sur ZIP qui doit avoir un fichier META-INF/container.xml qui décrit le point de départ de la version MusicXML du fichier. Aucun fichier .xsd correspondant n'est défini pour le format de fichier MXL.

Un simple fichier container.xml a le contenu suivant. Cet exemple est tiré du fichier Dichterliebe01.mxl disponible sur le site Web MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Dans cet exemple, le<container> element est l'élément du document. La<rootfiles> l'élément peut contenir un ou plusieurs<rootfile> éléments, avec le premier<rootfile> élément décrivant la racine MusicXML. Un fichier MusicXML utilisé comme<rootfile> puis-je avoir<score-partwise> ,<score-timewise> , ou<opus> comme élément de document.

## Références

* [Fichiers MXL compressés] (https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC1951](https://www.ietf.org/rfc/rfc1951.txt)

