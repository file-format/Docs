---
date: 2019-10-11
keywords: prc, .prc, format de fichier prc, comment ouvrir les fichiers prc, extension .prc, extension prc
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier RPC
linktitle: PRC
description: "Découvrez le format de fichier PRC et les API qui peuvent créer et ouvrir des fichiers PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Les formats de fichier PRC
Les extensions ".prc" sont utilisées pour le format de fichier Product Representation Compact 3D et un format de fichier e-book par MobiPocket.

## Qu'est-ce qu'un fichier Product Representation Compact (PRC) ?

PRC (Product Representation Compact) est un format de fichier 3D optimisé pour stocker, charger et afficher des données 3D provenant notamment de systèmes de CAO (conception assistée par ordinateur). C'est un fichier binaire séquentiel, écrit de manière portable. PRC peut être utilisé pour intégrer des données 3D dans un fichier PDF. PRC prend en charge la plupart des constructions principales de la CAO telles que les assemblages et les pièces, les arbres d'entités 3D, la représentation géométrique exacte, la représentation triangulée et le balisage. PRC utilise l'extension .prc et le type de média Internet utilisé est *model/prc*.

PRC est un format de fichier polyvalent qui, en fonction de son utilisation, peut soit être stocké à l'aide d'une compression régulière pour représenter directement les données CAO, soit être stocké à l'aide d'une compression élevée pour réduire la taille du fichier. Les données 3D stockées dans un PDF au format PRC sont interopérables avec les applications CAM et CAE.

### Spécification du format de fichier Compact Representation Compact (PRC)

Un fichier PRC a une section d'en-tête principale suivie d'une ou plusieurs structures de fichiers suivies d'un fichier modèle à la fin. Une structure de fichier comporte un en-tête suivi des sections de données suivantes :

- **Globals** : il contient les structures et les couleurs de fichier référencées, les styles de ligne et les systèmes de coordonnées pour chaque entité arborescente de la structure de fichier.
- **Arbre** : il contient une description de l'arborescence des éléments tels que les occurrences de produit, les définitions d'articles, les éléments de représentation et le balisage.
- **Tessellation** : Il contient toutes les données tessellées (triangulées) dans les entités feuilles de l'arbre (éléments de représentation et balises).
- **Géométrie** : Il contient toutes les données exactes de géométrie et de topologie des entités feuilles de l'arbre (éléments de représentation).
- **Géométrie supplémentaire** : Il contient les données récapitulatives de la géométrie. Cela permet au fichier d'être partiellement chargé sans charger toute la géométrie.

Voici la structure d'un fichier PRC typique.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Qu'est-ce qu'un fichier de livre électronique MobiPocket avec l'extension PRC
Un format de fichier de livre électronique introduit par une société française appelée **Mobipocket** utilise également l'extension ".prc". Initialement, le Mobipocket a lancé une application gratuite pour plusieurs appareils intelligents tels que les tablettes, les PDA et les smartphones. L'extension ".prc" est en fait identique à .mobi mais est particulièrement utilisée pour les PDA qui ne supportent que les extensions **.prc** ou **.pdb**.

### Spécifications du format de fichier Mobipocket PRC
Le format de fichier MobiPocket PRC est basé sur la norme Open eBook utilisant XHTML et peut également inclure JavaScript et des cadres. La prise en charge des requêtes SQL natives à utiliser avec les bases de données intégrées est également disponible.

Le Mobipocket Reader dispose d'une bibliothèque de page d'accueil. Les lecteurs peuvent insérer des pages vierges dans n'importe quelle partie d'un livre et ajouter des dessins variables. Les objets tels que les annotations, les signets, les corrections, les notes et les dessins sont gérables à partir d'un seul emplacement. Les images sont converties au format GIF et ont une taille maximale de 64K, ce qui est suffisant pour les téléphones portables avec de petits écrans. Mobipocket Reader a les signets électroniques et un dictionnaire intégré.

Le lecteur dispose d'un mode plein écran pour la lecture et prend en charge de nombreux PDA, communicateurs et smartphones. Les produits Mobipocket prennent en charge la plupart des systèmes d'exploitation Palm, Windows, Symbian, BlackBerry, mais pas Android. Le lecteur fonctionne sous Linux ou Mac OS X en utilisant WINE.

## Références

- [RPC - Wikipédia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Spécification du format RPC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparaison des formats de livres électroniques - Par Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

