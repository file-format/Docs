---
date: 2020-08-12
keywords: flif, .flif, format de fichier flif, comment ouvrir des fichiers flif, extension .flif, extension flif
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier FLIF
linktitle: FLIF
description: "Découvrez le format de fichier FLIF et les API qui peuvent créer et ouvrir des fichiers FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Qu'est-ce qu'un fichier FLIF ? ##

FLIF (Free Lossless Image Format) est un format d'image sans perte qui utilise l'extension .flif pour ses fichiers. FLIF prétend surpasser [PNG](/fr/image/png/), [WebP](/fr/image/webp/) sans perte, BPG sans perte et JPEG 2000 sans perte en termes de taux de compression. FLIF utilise un entrelacement progressif, grâce auquel tout téléchargement partiel de l'image peut être utilisé comme codage avec perte pour l'image entière.

## Bref historique ##

FLIF a été annoncé en septembre 2015 et la version alpha a été publiée en octobre 2015. En septembre 2016, la première version stable de FLIF a été publiée.

## Conception FLIF ##

FLIF utilise une variante de CABAC (context-adaptive binary arithmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) pour la compression. MANIAC est un algorithme de codage entropique développé par Jon Sneyers et Pieter Wuille. Dans MANIAC, les contextes sont des nœuds d'arbres de décision qui sont appris dynamiquement au moment de l'encodage. Cela rend le modèle de contexte plus spécifique à l'image et se traduit par une meilleure compression. FLIF a les caractéristiques suivantes :

- Prend en charge la compression sans perte
- Prend en charge la compression avec perte avec prétraitement de l'encodeur
- Prend en charge les niveaux de gris, RVB et RVBA
- Prend en charge la profondeur de couleur de 1 à 16 bits par canal
- Prend en charge les fichiers entrelacés et non entrelacés
- Prend en charge le décodage progressif des fichiers partiellement téléchargés
- Prend en charge les animations
- Prend en charge les profils de couleur ICC intégrés, les métadonnées Exif et XMP
- A un support limité pour la compression des fichiers bruts de l'appareil photo (RGGB)

## Format de fichier FLIF ##

Un fichier FLIF comporte les quatre parties suivantes :

## En-tête principal ##

L'en-tête principal contient les principales métadonnées, y compris la largeur, la hauteur, la profondeur de couleur, le nombre d'images.

|Type|Valeur|Description|
|---|---|---|
|4 octets|"FLIF"|Magique|
|4 bits|3 = ni encore ; 4 = je encore ; 5 = ni anim ; 6 = i anim|Entrelacement, animation|
|4 bits|1 = Niveaux de gris ; 3 = RVB ; 4 = RVBA|Nombre de canaux (nb_canaux)|
|1 octet|'0','1','2' ('0'=personnalisé)|Octets par canal (Bpc)|
|varint|largeur-1|Largeur|
|varint|hauteur-1|Hauteur|
|varint|nb_frames-2 (uniquement si animation)|Nombre d'images (nb_frames)|

## Morceaux de métadonnées ##

Cette partie contient des métadonnées non-pixel comme Exif/XMP, le profil de couleur ICC, etc. qui est encodé à l'aide de la compression DEFLATE. Ces morceaux sont définis de la même manière que les morceaux PNG, la différence étant que la taille du mandrin est codée avec un nombre variable d'octets. Les noms des blocs peuvent être de 4 lettres (4 octets) ou une valeur inférieure à 32 indiquant un bloc non facultatif.

Voici un exemple de mandrins optionnels :

|Nom du bloc|Description|Contenu (après décompression DEFLATE)|
|---|---|---|
|iCCP|Profil de couleur ICC|données brutes du profil de couleur ICC|
|eXif|Métadonnées Exif|En-tête "Exif\0\0" suivi d'un en-tête TIFF et des données EXIF|
|eXmp|Métadonnées XMP|XMP contenu dans un xpacket en lecture seule sans remplissage|

### Convention de dénomination ###

- **Première lettre** : les majuscules sont utilisées pour les blocs critiques et les minuscules sont utilisées pour les blocs non critiques.
- **Deuxième lettre** : les majuscules sont utilisées pour les parties publiques et les minuscules sont utilisées pour les parties privées
- **Troisième lettre** : les majuscules sont utilisées pour les mandrins nécessaires à l'affichage correct de l'image et les minuscules ne sont pas importantes pour afficher l'image.
- **Quatrième lettre** : la majuscule est utilisée pour les mandrins qui peuvent être copiés à l'aveugle en toute sécurité. Les mandrins en minuscules dépendent des données d'image.

## Deuxième en-tête ##

Celui-ci contient les informations concernant le codage réel des pixels.

|Type|Description|Condition|Valeur par défaut|
|---|---|---|---|
|1 octet|octet NUL (0x00), nom de bloc d'un flux binaire FLIF16||
|uni_int(1,16)|Bits par pixel des canaux|Bpc == '0' : répéter(nb_canaux)|8 si Bpc == '1', 16 si Bpc == '2'|
|uni_int(0,1)|Indicateur : alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Nombre de boucles|nb_frames > 1||
|uni_int(0,60_000)|Délai de trame en ms|nb_frames > 1 : répéter(nb_frames)|
|uni_int(0,1)|Indicateur : has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|diviseur alpha|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Drapeau : has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variable|Transformations (voir ci-dessous)|||
|uni_int(1) = 0|Bit indicateur : terminé avec transformations|||
|uni_int(0,2)|Prédicteur de pixels invisibles|alpha_zero && entrelacé && la plage alpha inclut zéro||

**Chaînes**

|Numéro de canal|Description|
|---|----|
|0|Rouge ou Gris|
|1|Vert|
|2|Bleu|
|3|Alpha|

**Transformations**

|Type|Description|
|---|---|
|uni_int(1) = 1|Bit indicateur : pas encore fait|
|uni_int(0,13)|Identifiant de transformation|
|variable|Données de transformation (dépend de la transformation)|

La transformation est utilisée pour modifier les données de pixel pour une meilleure compression et pour garder une trace des valeurs de pixel réelles.

## Données de pixels ##

Cette partie contient les données de pixel réelles codées à l'aide du codage entropique MANIAC. Les pixels peuvent être codés à l'aide d'un codage entrelacé ou non entrelacé.

### Méthode entrelacée ###

Dans cette méthode, les niveaux de zoom sont définis. Le niveau de zoom 0 est utilisé pour l'image complète, le niveau de zoom 1 est utilisé pour toutes les lignes paires, le niveau de zoom 2 est utilisé pour toutes les colonnes paires du niveau de zoom 1. En d'autres termes, chaque niveau de zoom pair 2k est une version sous-échantillonnée du image, à l'échelle 1:2^k. Les niveaux de zoom sont codés du plus élevé au plus bas.

### Méthode non entrelacée ###

Dans cette méthode, le codage des arbres MANIAC commence immédiatement suivi du codage des pixels.

## Références ##

- [FLIF - Wikipédia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

