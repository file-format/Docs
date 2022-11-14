---
date: 2020-08-12
keywords: jfif, .jfif, format de fichier jfif, comment ouvrir les fichiers jfif, extension .jfif, extension jfif
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Fichier JFIF - Qu'est-ce qu'un fichier .jfif ?
linktitle: JFIF
description: "Découvrez le format de fichier JFIF et les API qui peuvent créer et ouvrir des fichiers JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Qu'est-ce qu'un fichier JFIF ?

JFIF (JPEG File Interchange Format (JFIF)) est un fichier de format d'image qui utilise l'extension .jfif. JFIF s'appuie sur JIF (JPEG Interchange Format) en réduisant la complexité et en résolvant ses limites.

## Bref historique de JFIF

Le développement du document JFIF a été dirigé par Eric Hamilton et un accord sur la première version a été établi à la fin de 1991. La version 1.02 a été publiée le 7 septembre 1992. La RFC 2046 spécifiait que le format JFIF est utilisé pour transmettre des images JPEG sur Internet. Le JFIF a été publié par l'ECMA en 2009 et a été normalisé par l'UIT-T en 2011 sous le nom de Recommandation T.871 et par l'ISO/CEI en 2013 sous le nom d'ISO/CEI 10918-5

## Format de fichier JFIF ##

Un fichier JFIF consiste en une séquence de marqueurs tels que définis dans la partie 1 de la norme JPEG. Chaque marqueur est constitué de deux octets (FF suivi d'un octet qui spécifie le type de marqueur). Les marqueurs peuvent être autonomes ou indiquer le début d'un segment marqueur.

JFIF permet à plusieurs composants comme Y, Cb, Cr, d'avoir des résolutions différentes mais leur alignement n'est pas défini. Contrairement à JPEG, JFIF peut fournir des informations sur la résolution et le format d'image. JFIF définit également le modèle de couleur à utiliser.

### Structure du fichier ##

|Segment|Code|Description|
|---|---|---|
|SOI|FF D8|Début de l'image|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segments marqueurs supplémentaires|
|SOS|FF DA|Début de l'analyse|
||données d'image compressées||
|EOI|FF D9|Fin de l'image|

La norme JFIF définit les segments suivants :

### Segment marqueur JFIF APP0 ###

Il s'agit d'un segment obligatoire contenant des paramètres d'image. Il peut également contenir une vignette intégrée non compressée.

|Champ|Taille (octets)|Description|
|---|---|---|
|APP0 marqueur|2|FF E0|
|Longueur|2|Longueur du segment sans le marqueur APP0|
|Identifiant|5|JFIF (4A 46 49 46 00) en ASCII terminé par un octet nul|
|Version JFIF|2|Version du JFIF|
|Unités de densité|1|Unité pour les champs de densité de pixels suivants</br> 00 : Aucune unité ; le rapport hauteur/largeur des pixels est égal à Ydensity:Xdensity</br> 01 : Pixels par pouce</br> 02 : Pixels par centimètre |
|Xdensity|2|Densité de pixels horizontale supérieure à zéro|
|Ydensity|2|Densité de pixels verticale supérieure à zéro|
|Xthumbnail|1|Nombre de pixels horizontaux de la vignette RVB intégrée. Peut être zéro |
|Ythumbnail|1|Nombre de pixels verticaux de la vignette RVB intégrée. Peut être zéro |
|Données de vignettes|3 × n|Données de vignettes raster RVB 24 bits non compressées|

### Segment marqueur APP0 d'extension JFIF ###

Il s'agit d'une section facultative qui, si elle est définie, doit suivre immédiatement le segment marqueur JFIF APP0. Cette section est prise en charge par JFIF version 1.02 et supérieure et permet l'intégration de vignettes dans trois formats différents.

|Champ|Taille (octets)|Description|
|---|---|---|
|APP0 marqueur|2|FF E0|
|Longueur|2|Longueur du segment hors marqueur APP0|
|Identifiant|5|JFXX (4A 46 58 58 00) en ASCII terminé par un octet nul|
|Format de vignette|1|Spécifie le format de données utilisé pour la vignette intégrée suivante :</br> 10 : Format JPEG</br> 11 : 1 octet par pixel format palettisé</br> 13 : 3 octets par pixel format RVB |
|Données miniatures|variable||

## Conversion de JFIF vers d'autres formats de fichiers image

JFIF peut être converti en formats de fichiers image populaires tels que [PNG](/fr/image/png/), [JPG](/fr/image/jpg/) et [PDF](/fr/pdf/).

## Références ##

- [JFIF - Wikipédia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

