{
  "date" : "2019-10-11",
  "keywords" :[ "fichier ico", "format de fichier ico", "qu'est-ce qu'un fichier ico", "fichier", "exemple ico", "extension de fichier ico","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Format de fichier image",
  "description":"En savoir plus sur le format de fichier ICO et les API qui peuvent créer et ouvrir des fichiers ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier ICO ?

Les fichiers avec l'extension ICO sont des types de fichiers image utilisés comme icône pour la représentation d'une application sur [Microsoft Windows](https://www.microsoft.com/en-us/windows). Ceux-ci sont disponibles en différentes tailles, couleurs et résolutions pour répondre aux exigences de l'affichage. Un autre format de fichier image similaire sur Microsoft Windows est [CUR](/fr/image/cur/) pour la représentation du curseur et définit un hotspot dans l'en-tête de l'image. Sur MacOS, les formats de fichiers ICNS ont le même objectif que les fichiers ICO. Plusieurs sites Web en ligne ainsi que des applications offrent la possibilité de créer de tels fichiers et de convertir d'autres formats d'image tels que [BMP](/fr/image/bmp/), [PNG](/fr/image/png/), etc. au format de fichier icône. Le type de média Internet officiel enregistré par l'IANA pour les fichiers ICO est image/vnd.microsoft.icon.

## Bref historique ##

Les icônes ont été introduites avec le lancement de Microsoft Windows 1.0. Celles-ci étaient de taille 32x32 et étaient monochromes. Avec l'arrivée de win32, la prise en charge des images d'icônes en couleurs vraies a été introduite avec jusqu'à 256x256 pixels de dimension. Windows XP a été le premier à prendre en charge les images d'icônes couleur 32 bits, permettant d'ajouter à l'icône des zones semi-transparentes telles que les ombres, l'anticrénelage et les effets de type verre. Microsoft ne recommande que des tailles d'icônes jusqu'à 48 × 48 pixels pour Windows XP. Windows Vista a ajouté une vue d'icônes de 256 × 256 pixels à l'Explorateur Windows, ainsi que la prise en charge du format compressé [PNG] (/fr/image/png/). Avec les utilisateurs utilisant des résolutions plus élevées et des modes DPI élevés, des formats d'icônes plus grands (tels que 256 × 256) sont recommandés.

## Format de fichier ICO ##

Un seul fichier ICO se compose d'une ou plusieurs petites images de plusieurs tailles et profondeurs de couleur. La présence d'images de plusieurs tailles permet une mise à l'échelle appropriée à différentes résolutions d'écran. Toutes les valeurs des fichiers ICO/CUR sont représentées dans l'ordre des octets [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Le fichier ICO se compose d'un en-tête d'icône, d'un répertoire d'icônes,

|Champ|Description
---|---|
|Icon Header|Stocke des informations générales sur le fichier ICO.
|Directory[1..n]|Stocke des informations générales sur chaque image du fichier.
|Icône #1|Les "données" réelles pour la première image dans l'ancien format AND/XOR DIB ou PNG plus récent
|...|
|Icon #n|Données de la dernière image d'icône

### Entête ###

|Décalage|Taille (en octets)|Objectif
---|---|---|
|0|2|Réservé. Doit toujours être 0.
|2|2|Spécifie le type d'image : 1 pour l'image d'icône (.ICO), 2 pour l'image de curseur (.CUR). Les autres valeurs ne sont pas valides.
|4|2|Spécifie le nombre d'images dans le fichier.

### Répertoire ###

Le répertoire contenu dans un fichier ICO, représenté par la structure ICONDIR, contient une structure ICONDIRECTORY pour chaque image du fichier. Le même est suivi d'un bloc contigu de toutes les données bitmap d'image. C'est comme indiqué ci-dessous.

|Décalage|Taille|Description
---|---|---|
|0 (0)|1|Largeur, devrait être 0 si 256 pixels
|1 (1)|1|Hauteur, doit être 0 si 256 pixels
|2 (2)|1|Nombre de couleurs, doit être 0 si plus de 256 couleurs
|3 (3)|1|Réservé, devrait être 0
|4 (4)|2|Les plans de couleur au format .ICO doivent être 0 ou 1, ou le point chaud X au format .CUR
|6 (6)|2|Bits par pixel au format .ICO, ou point d'accès Y au format .CUR
|8 (8)|4|Taille des données bitmap en octets.
|12 (C)|4|Décalage dans le fichier.

## Références ##

* [ICO - Par Wikipédia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

