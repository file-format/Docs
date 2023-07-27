{
  "date" : "2019-10-11",
  "keywords" :[ "fichier bmp", "format de fichier bmp", "qu'est-ce qu'un fichier bmp", "fichier", "exemple bmp", "extension de fichier bmp","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Format de fichier image",
  "description":"En savoir plus sur le format de fichier BMP et les API qui peuvent créer et ouvrir des fichiers BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Qu'est-ce qu'un fichier BMP ? #

Les fichiers ayant l'extension .BMP représentent des fichiers d'image bitmap utilisés pour stocker des images numériques bitmap. Ces images sont indépendantes de la carte graphique et sont également appelées format de fichier bitmap indépendant du périphérique (DIB). Cette indépendance sert à ouvrir le fichier sur plusieurs plates-formes telles que Microsoft Windows et Mac. Le format de fichier BMP peut stocker des données sous forme d'images numériques bidimensionnelles au format monochrome et couleur avec différentes profondeurs de couleur.

## Spécifications du format de fichier BMP ##

Les bitmaps indépendants du périphérique agissent comme une aide à l'échange de bitmaps entre les périphériques et les applications. En raison de l'évolution continue de ce format de fichier, les informations contenues dans les en-têtes peuvent être différentes selon la version de Bitmap. Un seul fichier bitmap se compose de structures fixes et de tailles variables dans une séquence spécifique.

Les structures d'un fichier Bitmap sont organisées dans l'ordre suivant :


|Structure|Facultatif|Taille|Objectif
---|---|---|---|
|En-tête de fichier|Non|14|Pour stocker des informations générales sur le fichier image bitmap
|En-tête DIB|Non|Taille fixe|Pour stocker des informations détaillées sur l'image bitmap et définir le format de pixel
|Extra Bit Masks|Oui|12 ou 16 octets|Pour définir le format de pixel
|Palette de couleurs|Semi-facultatif|Taille variable|Pour définir les couleurs utilisées par les données d'image bitmap
|Gap1|Oui|Taille variable|Alignement de la structure
|Pixel Array|No|Variable-size|Le format de pixel est défini par l'en-tête DIB ou les masques de bits supplémentaires.
|Gap2|Oui|Taille variable|Alignement de la structure
|Profil de couleur ICC|Oui|Taille variable|Pour définir le profil de couleur pour la gestion des couleurs

Lorsqu'une image bitmap est chargée en mémoire, elle devient une structure DIB, utilisée par Windows via son API GDI. L'en-tête de fichier ne fait pas partie de cette structure de données. La couleur peut également être constituée d'entrées 16 bits qui constituent des index de la palette actuellement référencée au lieu de définitions de couleurs RVB explicites. Examinons certains d'entre eux en détail, en particulier les en-têtes.

### En-tête de fichier bitmap ###

Un en-tête de fichier bitmap est similaire aux autres en-têtes de fichier utilisés pour identifier le fichier. Puisqu'il existe différentes variantes du format de fichier BMP, les 2 premiers octets du format de fichier BMP sont le caractère "B" puis le caractère "M" en codage ASCII. Toutes les valeurs entières sont stockées au format little-endian.

|Décalage hex|Décalage déc|Taille|Objectif
---|---|---|---|
|00|0|2 octets|Le champ d'en-tête utilisé pour identifier le fichier BMP et DIB est 0x42 0x4D en hexadécimal, identique à BM en ASCII. Il peut suivre les valeurs possibles.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2 struct bitmap array * **CI** – OS/2 struct icône de couleur * **CP** – pointeur de couleur const OS/2 * **IC** – icône de structure OS/2 * **PT** – pointeur OS/2
|02|2|4 octets|La taille du fichier BMP en octets
|06|6|2 octets|Réservé ; la valeur réelle dépend de l'application qui crée l'image
|08|8|2 octets|Réservé ; la valeur réelle dépend de l'application qui crée l'image
|0A|10|4 octets|Le décalage, c'est-à-dire l'adresse de début, de l'octet où se trouvent les données d'image bitmap (pixel array).

#### En-tête DIB (en-tête d'informations bitmap) ####

Les informations détaillées sur l'image sont représentées par cet en-tête. Sur la base de ces informations, l'application sera déterminée qui sera utilisée pour afficher l'image sur l'écran. Tous ces en-têtes contiennent un champ DWORD (32 bits), spécifiant leur taille, afin qu'une application puisse facilement déterminer l'en-tête utilisé dans l'image. Ceci est essentiellement dû au fait que le format DIB a subi plusieurs extensions. Voici l'en-tête DIB avec les champs répertoriés.

#### Palette de couleurs ####

Une palette de couleurs BMP est un tableau de structures qui spécifient les valeurs d'intensité RVB de chaque couleur dans la palette de couleurs d'un périphérique d'affichage. Chaque pixel des données bitmap stocke une valeur unique utilisée comme index dans la palette de couleurs. Les informations de couleur stockées dans l'élément à cet index spécifient la couleur de ce pixel. La disponibilité de la couleur dans un fichier bitmap varie comme suit :

* Un, 4 et 8 bits - devrait toujours contenir une palette de couleurs
* Seize, 24 et 32 bits - ne contiennent jamais de palettes de couleurs
* Fichiers BMP 16 et 32 bits - contiennent des valeurs de masque de champs de bits à la place de la palette de couleurs

#### Stockage de pixels ####

Les pixels bitmap sont stockés sous forme de bits regroupés en lignes où la taille de chaque ligne est arrondie à un multiple de 4 octets (un DWORD 32 bits) par remplissage. La quantité totale d'octets nécessaires pour stocker les pixels d'une image ne peut pas être calculée directement en comptant simplement les bits. Puisqu'il y a du remplissage impliqué, l'effet d'arrondir la taille de chaque ligne à un multiple de 4 octets est requis. Les octets de bourrage (pas nécessairement 0) doivent être ajoutés à la fin des lignes afin de porter la longueur des lignes à un multiple de quatre octets. Lorsque le tableau de pixels est chargé en mémoire, chaque ligne doit commencer à une adresse mémoire multiple de 4.

L'image est en fait décrite par la représentation DWORD 32 bits du tableau de pixels. Habituellement, les pixels sont stockés "de bas en haut", en commençant par le coin inférieur gauche, en allant de gauche à droite, puis ligne par ligne du bas vers le haut de l'image. Les formats de pixels et leurs implications sont répertoriés ci-dessous :

* Le format 1 bit par pixel (1bpp) prend en charge 2 couleurs distinctes (par exemple : noir et blanc).
* Le format 2 bits par pixel (2bpp) prend en charge 4 couleurs distinctes et stocke 4 pixels par 1 octet, le pixel le plus à gauche étant dans les deux bits les plus significatifs. Chaque valeur de pixel est un index de 2 bits dans une table de 4 couleurs maximum.
* Le format 4 bits par pixel (4bpp) prend en charge 16 couleurs distinctes et stocke 2 pixels par 1 octet, le pixel le plus à gauche étant dans le quartet le plus significatif. Chaque valeur de pixel est un index de 4 bits dans une table de 16 couleurs maximum.
* Le format 8 bits par pixel (8bpp) prend en charge 256 couleurs distinctes et stocke 1 pixel par 1 octet. Chaque octet est un index dans une table contenant jusqu'à 256 couleurs.
* Le format 16 bits par pixel (16 bpp) prend en charge 65 536 couleurs distinctes et stocke 1 pixel par MOT de 2 octets. Chaque MOT peut définir les échantillons alpha, rouge, vert et bleu du pixel.
* Le format de pixel 24 bits (24bpp) prend en charge 16 777 216 couleurs distinctes et stocke 1 valeur de pixel par 3 octets. Chaque valeur de pixel définit les échantillons rouge, vert et bleu du pixel (8.8.8.0.0 en notation RGBAX). Plus précisément, dans l'ordre : bleu, vert et rouge (8 bits pour chaque échantillon).
* Le format 32 bits par pixel (32 bpp) prend en charge 4 294 967 296 couleurs distinctes et stocke 1 pixel par DWORD de 4 octets. Chaque DWORD peut définir les échantillons alpha, rouge, vert et bleu du pixel.

## Références ##

* [Format de métafichier Windows](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Format de fichier BMP](https://en.wikipedia.org/wiki/BMP_file_format)

