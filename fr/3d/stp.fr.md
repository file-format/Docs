---
date: 2022-01-31
keywords: stp, .stp, format de fichier stp, comment ouvrir les fichiers stp, extension .stp, extension stp
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fichier STP
linktitle: STP
description: "Découvrez le format de fichier STP et les API qui peuvent créer et ouvrir des fichiers STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Qu'est-ce qu'un fichier STP ?

Un fichier STP est un fichier CAO 3D utilisé pour l'échange de données produit entre les applications CAO et FAO. Il contient des informations sur les objets 3D et est enregistré de la même manière que le format de fichier **STEP**. Les fichiers STP facilitent l'échange de données entre les applications conformément aux protocoles d'application [STEP](/fr/3d/step/) ISO 10303-2xx. Cette norme ISO définit le mécanisme de codage pour la représentation des données dans le langage de modélisation de données EXPRESS. Les fichiers STP peuvent être ouverts dans des applications telles que **Autodesk Fusion 360**.

## Format de fichier STP - Plus d'informations

Les fichiers STP sont enregistrés sur le disque au format de fichier ASCII brut. Ceux-ci contiennent des informations sur les modèles 3D sous forme de texte brut qui peuvent être lus par les applications CAD/CAM pour charger ces modèles.

Les fichiers STP sont également enregistrés avec l'extension .step et consistent en une séquence d'enregistrements. Les principales caractéristiques de ces fichiers incluent :

* Le jeu de caractères est défini comme points de code de la norme ISO 10646.
* "ISO-10303-21 ;" sont les premiers caractères du premier enregistrement.
* Les commentaires sont entourés des caractères "/*" et "*/".
* Le dernier enregistrement contient "END-ISO-10303-21 ;" si le fichier STEP est conforme à la version 2002.
* Dans le cas où il est conforme à la version 2016, il peut y avoir une ou plusieurs signatures numériques après le "END-ISO-10303-21 ;" terminateur.
* Les sauts de ligne sont indiqués par "\N\" et les sauts de page sont indiqués par "\F\".

## Ouvrir les fichiers STP

Les fichiers STP peuvent être ouverts dans les visualiseurs STP ainsi que dans les éditeurs de texte.

### Ouvrir les fichiers STP avec les visualiseurs STP

Diverses applications de CAO peuvent ouvrir des fichiers STP pour les afficher sous Windows, MacOS et Linux. Ceux-ci inclus:

* Autodesk Fusion 360 (multiplateforme)
* FreeCAD (multiplateforme)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systèmes CATIA (Windows, Linux)

### Ouvrir les fichiers STP avec des éditeurs de texte

Les fichiers STP sont enregistrés sous forme de fichiers texte brut. Cela permet d'ouvrir les fichiers STP avec des éditeurs de texte. Les éditeurs de texte populaires tels que le Bloc-notes et le Bloc-notes ++ sur le système d'exploitation Windows et Apple TextEdit sur MacOS peuvent ouvrir les fichiers STP. Une fois ouvert dans un éditeur de texte, l'utilisateur peut modifier les propriétés du fichier STP. Cependant, cela peut entraîner une corruption du fichier en cas de mise à jour incorrecte des propriétés.

## Comment convertir les fichiers STP

Il existe plusieurs applications qui peuvent convertir des fichiers STP vers d'autres formats de fichiers. Les applications CAO capables de convertir les fichiers STP incluent :

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

En plus de cela, il existe plusieurs applications en ligne qui peuvent convertir des fichiers STP en d'autres formats de fichiers. Ces applications en ligne vous permettent de télécharger votre fichier STP sur des serveurs cloud où il est converti au format souhaité et renvoyé pour téléchargement.

Autodesk Fusion 360 peut convertir des fichiers STP aux formats de fichiers 3D et CAO suivants.

* [OBJ](/fr/3d/obj/)
* [3MF](/fr/3j/3mf/)
* [DWG](/fr/cad/dwg/)
* [DXF](/fr/cad/dxf/)
* [ASM](/fr/cad/asm/)
* [IGES](/fr/cad/iges/)
* [STL](/fr/cad/stl/)
* [FBX](/fr/3d/fbx/)
* F3D
* [USD](/fr/3j/USD/)

## Références

* [ISO 10303-21 - Wikipédia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

