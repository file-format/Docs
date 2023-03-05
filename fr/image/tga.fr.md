{
  "date" : "2019-10-11",
  "keywords" :[ "fichier tga", "format de fichier tga", "qu'est-ce qu'un fichier tga", "fichier", "exemple tga", "extension de fichier tga","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier TGA - Un fichier d'image graphique TARGA",
  "description":"En savoir plus sur le format de fichier TGA et les API qui peuvent créer et ouvrir des fichiers TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier TGA ?

Un fichier avec l'extension .tga est un format graphique raster et a été créé par Truevision Inc. Il a été conçu pour les cartes TARGA (Truevision Advanced Raster Adapter) et a fourni la prise en charge de l'affichage Highcolor/truecolor pour les PC compatibles IBM. Il prend en charge 8, 16, 24 et 32 bits par pixel et un canal alpha 8 bits. Il prend également en charge la compression RLE sans perte qui peut être appliquée pour réduire la taille de l'image. Les photos et textures numériques utilisent le format d'image TGA.

## Bref historique

La formation du format de fichier TGA a vu le jour en 1984 par AT&T EPICenter (plus tard extrait et formé en tant qu'entité indépendante connue sous le nom de Truevision) qui travaillait sur la commercialisation de nouvelles technologies développées par AT&T pour les tampons de trame couleur. EPICenter travaillait déjà sur ses deux premières cartes, la VDA (Video Display Adapter) et l'ICB (image capture board) pour lesquelles le travail sur deux types de fichiers, .vda et .icb, était déjà en cours. Ces formats de fichiers ont été codifiés et un format de fichier spécifique moins large TGA a été introduit. TGA était une extension de ce qui était déjà utilisé et fournissait des informations telles que la largeur, la hauteur, la profondeur des pixels, la carte de couleurs associée et l'origine de l'image.

La version 2.0 de TGA, publiée en 1989, incorporait plusieurs fonctionnalités améliorées telles que :

* Vignettes
* Canal alpha
* Valeur gamma
* Métadonnées textuelles

Les principaux contributeurs à la version 2.0 de TGA incluent Shawn Steiner de Truevision, Kevin Fiedly et David Spoelstra.

## Spécifications du format de fichier TGA TARGA

Un fichier TGA se compose de 2 parties principales :

* Entête
* Informations sur les pixels de couleur

Toutes les valeurs d'un fichier TGA sont en littl-endian conformément aux spécifications de format.

### En-tête TGA

Un en-tête de fichier TGA se compose des 5 champs suivants.

|N° de champ|Longueur |Nom de champ |Description|
---|---|---|---|
|1| 1 octet |Longueur ID| Longueur du champ ID d'image (0-255) |
|2| 1 octet |Type de carte de couleurs| Si une palette de couleurs est incluse (0 - indique qu'aucune donnée de palette de couleurs n'est incluse avec cette image. 1 - indique qu'une palette de couleurs est incluse avec cette image.)|
|3| 1 octet |Type d'image| Types de compression et de couleur (0- Pas de données d'image incluses. 1- Non compressé, Image mappée en couleur, 2- Non compressé, Image en couleurs vraies, 9- Encodé en longueur, Image en couleur mappée, 11- Encodé en longueur, Image en noir et blanc )|
|4| 5 octets |Spécification de la carte des couleurs| Décrit la carte des couleurs |
|5| 10 octets |Spécification d'image| Dimensions et format de l'image |

### Données d'image et de carte de couleurs

|Champ no. |Longueur |Champ |Description|
---|---|---|---|
|6 |Depuis le champ de longueur de l'ID d'image| ID d'image| Champ facultatif contenant des informations d'identification |
|7 |Depuis le champ de spécification de la carte des couleurs| Données cartographiques en couleur | Table de recherche contenant des données de carte de couleur |
|8 |Depuis le champ de spécification d'image| Données d'image| Stocké selon le descripteur d'image|

### Espace développeur (facultatif)

La version 2.0 de TGA prend en charge les améliorations/extras supplémentaires que de nombreux développeurs souhaitaient stocker plus d'informations. L'information est facultative de sorte que si un décodeur TGA n'est pas capable de l'interpréter, elle sera ignorée.

### Zone d'extension (facultatif)

|Numéro de champ| Longueur | Champ |Description|
---|---|---|---|
|10| 2 octets |Taille de l'extension |Taille en octets de la zone d'extension, toujours 495|
|11| 41 octets| Nom de l'auteur |Nom de l'auteur. S'ils ne sont pas utilisés, les octets doivent être définis sur NULL (\0) ou espaces|
|12| 324 octets | Commentaire de l'auteur | Un commentaire, organisé en quatre lignes, chacune composée de 80 caractères plus un NULL |
|13| 12 octets | Horodatage |Date et heure de création de l'image|
|14| 41 octets| ID de l'emploi||
|15| 6 octets | Temps de travail | Heures, minutes et secondes passées à créer le fichier (pour la facturation, etc.) |
|16| 41 octets| ID du logiciel |L'application qui a créé le fichier.|
|17| 3 octets | Version du logiciel||
|18| 4 octets | Couleur clé||
|19| 4 octets | Rapport d'aspect des pixels ||
|20| 4 octets | Valeur gamma||
|21| 4 octets | Décalage de la correction des couleurs |Nombre d'octets entre le début du fichier et la table de correction des couleurs si présente|
|22| 4 octets | Timbre-poste | Nombre d'octets entre le début du fichier et l'image du timbre-poste, le cas échéant |
|23| 4 octets | Décalage de la ligne de balayage | Nombre d'octets depuis le début du fichier jusqu'à la table des lignes de balayage si présente|
|24| 1 octet | Type d'attributs| Spécifie le canal alpha |

### Pied de page du fichier (facultatif)

Les 26 derniers octets du fichier représentent le pied de page, qui, s'il est présent, signifie qu'il s'agit probablement d'un fichier TGA version 2.

|Numéro de champ| Longueur | Champ | Descriptif|
---|---|---|---|
|28| 4 octets| Décalage d'extension| Décalage en octets depuis le début du fichier |
|29| 4 octets | Décalage de la zone développeur | Décalage en octets depuis le début du fichier |
|30| 16 octets| Signature | Contient "TRUEVISION-XFILE" |
|31| 1 octet | | Contient "." |
|32| 1 octet | | Contient NULL |


## Références

* [Spécifications du format de fichier TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA par Wikipédia](https://en.wikipedia.org/wiki/Truevision_TGA)

