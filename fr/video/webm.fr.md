---
date: 2019-10-11
keywords: WEBM, Qu'est-ce qu'un fichier WEBM, Format de fichier WEBM
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Découvrez le format de fichier WEBM et les API qui peuvent créer et ouvrir des fichiers WEBM."
title: WEBM - Format de fichier vidéo WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Qu'est-ce qu'un fichier WEBM ?

Un fichier avec une extension .webm est un fichier vidéo basé sur le format de fichier WebM ouvert et libre de droits. Il a été conçu pour le partage de vidéos sur le Web et définit la structure du conteneur de fichiers, y compris les formats vidéo et audio. WebM est 100% gratuit, mettant en œuvre une haute qualité basée sur des technologies ouvertes telles que HTML, HTTP et TCP/IP qui sont ouvertes à tous pour la mise en œuvre. WebM a été spécialement conçu pour diffuser des vidéos sur le Web, ce qui le rend optimisé pour le streaming avec une faible empreinte de calcul. Cela le rend adapté à la lecture de vidéos sur n'importe quel appareil, en particulier les netbooks, les ordinateurs de poche et les tablettes à faible consommation d'énergie.

## Format de fichier WEBM

La structure de fichier WebM est basée sur un sous-ensemble du format de fichier conteneur Matroska [MKV](/fr/video/mkv/). Les flux vidéo disponibles dans un fichier WebM sont compressés à l'aide des technologies de compression VP8 ou VP9 qui sont très efficaces en compression. De même, les flux audio d'un fichier WebM sont compressés à l'aide des codecs Vorbis ou Opus développés par la [Xiph Foundation](https://www.xiph.org/). Toutes ces vidéos et codecs audio sont libres de droits et peuvent être utilisés sans frais.

Voici les spécifications résumées du format de fichier WebM.

|Champ|Description|
---|---|
|type MIME |video/webm|
|Type MIME audio uniquement |audio/webm|
|Identifiant de type uniforme| org.webmproject.webm|
|Nom du codec vidéo| VP8 ou VP9|
|Nom du codec audio| Vorbis ou Opus|

### Éléments WebM

WebM, étant un sous-ensemble des spécifications Matroska, prend en charge certaines fonctionnalités de Matroska. Voici une description des éléments pris en charge.

#### EBML

|Nom |Description|
---|---|
|EBML|Définir les caractéristiques EBML des données à suivre. Chaque document EBML doit commencer par ceci.|
|EBMLVersion |La version de l'analyseur EBML utilisé pour créer le fichier.|
|EBMLReadVersion|La version minimale d'EBML qu'un analyseur doit prendre en charge pour lire ce fichier.|
|EBMLMaxIDLength |La longueur maximale des identifiants que vous trouverez dans ce fichier (4 ou moins dans Matroska).|
|EBMLMaxSizeLength|La longueur maximale des tailles que vous trouverez dans ce fichier (8 ou moins dans Matroska). Cela ne remplace pas la taille d'élément indiquée au début d'un élément. Les éléments dont la taille indiquée est supérieure à ce qui est autorisé par EBMLMaxSizeLength doivent être considérés comme non valides.|
|DocType|Une chaîne qui décrit le type de document qui suit cet en-tête EBML ("webm" dans notre cas).|
|DocTypeVersion|La version de l'interpréteur DocType utilisé pour créer le fichier.|
|DocTypeReadVersion|La version minimale de DocType qu'un interpréteur doit prendre en charge pour lire ce fichier.|

#### Éléments globaux

Pour le moment, seul l'élément `Void` est pris en charge pour annuler les données endommagées, afin d'éviter les comportements inattendus lors de l'utilisation de données endommagées. Le contenu est supprimé. Également utilisé pour réserver de l'espace dans un sous-élément pour une utilisation ultérieure.

#### Segment
Cet élément contient tous les autres éléments de niveau supérieur (niveau 1). Typiquement, un fichier Matroska est composé de 1 segment.

#### Informations de recherche de méta

Les informations de recherche suivantes sont prises en charge.

|Nom de l'élément |Description|
---|---|
|SeekHead |Contient la position d'un autre élément de niveau 1.|
|Recherche |Contient une seule entrée de recherche vers un élément EBML.|
|SeekID |L'ID binaire correspondant au nom de l'élément.|
|SeekPosition |La position de l'élément dans le segment en octets (0 = premier élément de niveau 1).|

## Références

* [WebM](https://www.webmproject.org/)
* [Référentiels de code WebM] (https://www.webmproject.org/code/#webp-repositories)

