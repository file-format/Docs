{
  "date" : "2019-10-11",
  "keywords" :[ "fichier psb", "format de fichier psb", "qu'est-ce qu'un fichier psb", "fichier", "exemple psb", "extension de fichier psb","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Format de fichier grande image Photoshop",
  "description":"En savoir plus sur le format de fichier PSB et les API qui peuvent créer et ouvrir des fichiers PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PSB ?
Adobe Photoshop enregistre les fichiers dans deux formats. Les fichiers ayant une taille de 30 000 par 30 000 pixels sont enregistrés avec l'extension PSD et les fichiers plus grands que PSD jusqu'à 300 000 par 300 000 pixels sont enregistrés avec l'extension PSB connue sous le nom de "Photoshop Big". Plus précisément, les fichiers PSB peuvent atteindre 4 Eb (plus de 4,2 milliards de Go) avec des images d'une hauteur et d'une largeur allant jusqu'à 300 000 pixels. Les PSD, en revanche, peuvent atteindre 2 Go maximum et des dimensions d'image de 30 000 pixels.

PSB est également connu sous le nom de format grand format pour Photoshop et prend en charge toutes les fonctionnalités de Photoshop telles que les calques, les effets et les filtres. Photoshop peut convertir le fichier PSB en [PSD](/fr/image/psd/), [JPG](/fr/image/jpeg/) , [PNG](/fr/image/png/), [EPS](/fr/page-description-language/eps/), [GIF](/fr/image/gif/) et d'autres formats également. Le format de document volumineux Photoshop est disponible une fois que la fonctionnalité du volet de gestion des fichiers de la boîte de dialogue des préférences de Photoshop est activée.

## Informations sur le format de fichier ##

Le format de fichier Photoshop est divisé en cinq parties principales avec de nombreux marqueurs de longueur pour se déplacer entre les sections.

|Format de fichier
---|
|En-tête de fichier
|Données du mode couleur
| Ressources d'images
|Informations sur les calques et les masques
|(((
Données d'image
)))

### En-tête de fichier ###

L'en-tête du fichier a une longueur fixe de 26 octets et contient les propriétés de base de l'image.

BYTE Signature [4] – Égal à '8BPS'.

WORD Version [2] – Numéro de version, PSD # 1, PSB # 2.

BYTE Réservé [6] – Réservé et toujours zéro.

WORD Channels [2] – Nombre de canaux de couleur dans l'image, y compris les canaux alpha. Sa valeur varie de 1 à 56.

LONG Rows [4] – Hauteur de l'image en pixels, PSD 1-30 000, PSB 1-300 000.

Colonnes LONGUES [4] – Largeur de l'image en pixels, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] – Nombre de bits par canal. Les valeurs prises en charge sont 1, 8, 16 et 32.

Mode WORD [2] – Mode couleur du fichier.

#### Mode Description ####


|Mode|Description
---|---|
|0|Bitmap (monochrome)
|1|Échelle de gris
|2|Indexé
|3|RVB
|4|CMJN
|7|Multicanal
|8|Duotone (demi-teinte)
|9|Laboratoire

### Données du mode couleur ###

Après la section d'en-tête de fichier, la section de données du mode couleur suit. Le bloc commence par un nombre LONG qui donne la longueur du bloc en octets. La structure des données du mode couleur est la suivante :

4 octets – La longueur des données de couleur suivantes.

Variable – Données de couleur

Si la valeur du champ de mode dans la section d'en-tête n'est pas Couleur indexée ou bichromie, la longueur du bloc sera de 0 et il n'y aura pas de données après le champ de longueur.

Pour les images couleur indexées, la longueur sera de 768 octets qui contiendront une palette de 256 couleurs. Pour le bichromie, les données contiendront les paramètres de l'écran et d'autres informations connexes.

### Ressources d'images ###

Après la section des données du mode couleur, le troisième bloc est la section des ressources d'image. Les quatre premiers octets sont un nombre LONG spécifiant la longueur du bloc suivi d'une série de blocs de ressources. La structure du bloc de ressources d'image est la suivante :

BYTE Type [4] – Signature '8BIM'

WORD ID [2] – ID de ressource d'image. Il existe une liste d'ID de ressources qui peut être consultée à partir du lien de référence.

BYTE Nom [Variable] – Nom : Chaîne Pascal de longueur paire. ** **

LONG Size [4] – Taille réelle des données de ressources qui suivent.

Données BYTE [Variable} – Données de ressource. Il est rembourré pour faire la même taille.

Certains des formats de ressources sont brièvement expliqués ci-dessous :

**Format des ressources de la grille et des guides :** Les informations de la grille et des guides sont stockées dans le bloc de ressources. Ces blocs de ressources contiennent une grille et un en-tête de guide de 16 octets suivis de blocs d'informations de guide de 5 octets.

**Format de ressource de vignette :** Les informations de vignette sont stockées dans le bloc de ressources d'image pour l'affichage de l'aperçu qui se compose d'un en-tête de 28 octets et d'une vignette JFIF en RVB.

**Format de ressource des échantillonneurs de couleur :** Les informations sur les échantillonneurs de couleur sont stockées dans un bloc de ressources d'image avec un en-tête de 8 octets suivi d'un bloc d'informations sur les échantillonneurs de couleur de longueur variable.

### Informations sur les calques et les masques ###

Le quatrième bloc est un bloc d'informations sur les calques et les masques et contient des informations sur les calques et les masques. Les informations de calque sont stockées en premier, puis les informations de masque.

**Informations sur le calque :** Les informations sur le calque commencent par une valeur LONG qui indique la longueur des informations sur le calque. Après cela, il y a le nombre de valeurs WORD qui indique le nombre d'enregistrements de couche à suivre.

[8] – longueur des couches

[2] - Nombre de couches

[Variable] – Informations sur chaque couche.

[Variable] – Données d'image du canal.** **

**Informations sur le masque :** La structure du masque a le format suivant :


|Structure de données|Nom de champ| La description
---|---|---|
|MOT| Superposer l'espace colorimétrique | (Non documenté)
|BYTE[8]| Composants de couleur| Composants de couleur 4x2 octets
|MOT| Opacité| 0#transparent, 1#opaque
|BYTE| Genre| 0 # inversé, 1 # protégé, 128 # utiliser la valeur stockée
|BYTE| rembourrage | mis à zéro

### Données d'image ###

La dernière section contient les données de pixel d'image. Les données d'image sont stockées sous la forme d'une série de séquences dans des plans, c'est-à-dire d'abord toutes les données rouges, puis toutes les données vertes, etc. WORD au début de chaque ligne indique la taille en octets liée à chaque ligne de balayage.

[2] – Méthode de compression :

[Variable] - Données d'image dans l'ordre planaire, c'est-à-dire RRRR, GGGG, BBBB, etc.

Méthodes de compression :

0 – Raw Données d'image

1 – RLE compressé

2 – Zip sans prédiction

3 – Zip avec prédiction

## Référence ##

* [Format de fichier PSB - Par Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipédia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

