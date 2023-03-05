{
  "date" : "2019-10-11",
  "keywords" :[ "fichier exif", "format de fichier exif", "qu'est-ce qu'un fichier exif", "fichier", "exemple exif", "extension de fichier exif","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"En savoir plus sur le format de fichier EXIF et les API qui peuvent créer et ouvrir des fichiers EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier EXIF ?
EXIF signifie "Exchangeable Image File Format", la définition donnée pour la première fois par [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) en 1985. La norme est gérée par Japan Electronics et Information Technology Industries Association (JEITA) à compter d'aujourd'hui. EXIF est une norme pour les spécifications des formats d'image et de son principalement utilisés par les appareils photo numériques et les scanners.

La norme EXIF inclut les informations de marquage et de métadonnées avec le fichier image. Les métadonnées peuvent contenir des informations telles que le modèle d'appareil photo, la vitesse d'obturation, la date et l'heure, l'ouverture, le fabricant, le temps d'exposition, la résolution X, la résolution Y, etc. Normalement, les données EXIF sont masquées par défaut. Pour afficher les données EXIF, il faut sélectionner les propriétés d'affichage dans l'application de visualisation d'images. Les métadonnées Exif peuvent également inclure des vignettes ainsi que des données d'image techniques et primaires dans un seul fichier image.

## Historique et Versions ##

* En octobre 1995, JEIDA a créé la version 1. Dans cette version, JEIDA a défini la structure, qui consiste en un format de données d'image et des informations d'attribut, et des balises de base.
* En novembre 1997, la version 1.1 a été introduite avec la plupart des balises de la version 1, mais a également ajouté des dispositions pour les informations d'attribut facultatives et le fonctionnement du format.
* Juin 1998, Version 2 avec espace colorimétrique sRGB, vignettes compressées et fichiers audio.
* Décembre 1998, Version 2.1 avec stockage amélioré et informations sur les attributs.
* Février 2002, Version 2.2, version 2.1 améliorée avec l'ajout de la finition d'impression.
* Septembre 2003, Version 2.21 avec espace colorimétrique optionnel connu sous le nom d'adobe RVB.

## Format de fichier EXIF

EXIF utilise les formats de fichiers suivants avec l'ajout de métadonnées spécifiques.

1. [JPEG](/fr/image/jpeg/) - transformée en cosinus discrète (DCT) pour les fichiers image compressés.
1. [TIFF](/fr/image/tiff/) Rev. 6.0 (RVB ou YCbCr) pour les fichiers image non compressés.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) pour les fichiers audio (Linéaire [PCM](https:/ /en.wikipedia.org/wiki/Pulse-code_modulation) ou ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM pour les données audio non compressées, et [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) pour les données audio compressées).

### Marqueur utilisé par EXIF ###

Le marqueur 0xFFE0~~0xFFEF est "Application Marker", utilisé par l'application utilisateur. Par exemple, les anciennes caméras numériques utilisent JFIF (JPEG File Interchange Format) pour stocker des images. JFIF utilise le marqueur APP0 (0xFFE0) pour insérer les données de configuration de la caméra numérique et l'image miniature. De plus, EXIF utilise également un marqueur d'application pour insérer des données, mais EXIF utilise le marqueur APP1 (0xFFE1) pour éviter un conflit avec le format JFIF. Tous les formats de fichiers EXIF commencent à partir de ce format.


|Marqueur SOI|Marqueur APP1|Données APP1|Autre marqueur
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Il commence à partir du marqueur SOI (0xFFD8), c'est donc un fichier JPEG. Ensuite, APP1 Marker suit immédiatement. Toutes les données d'EXIF sont stockées dans cette zone de données APP1. La partie "SSSS" sur le tableau supérieur signifie la taille de la zone de données APP1 (zone de données EXIF). Veuillez noter que la taille "SSSS" inclut également la taille du descripteur lui-même. Après le "SSSS", les données APP1 démarrent. La première partie est une donnée spéciale pour l'identification si EXIF ou non, le caractère ASCII "EXIF" et 2 octets de 0x00 sont utilisés. Après la zone du marqueur APP1, les autres marqueurs JPEG suivent.

### Structure de données Exif ###

Une structure approximative des données EXIF (APP1) est illustrée ci-dessous. Comme indiqué ci-dessus, les données EXIF commencent par le caractère ASCII "EXIF" et 2 octets de 0x00, puis les données EXIF suivent. EXIF utilise le format TIFF pour stocker les données.


|FFE1|APP1 Marqueur
---|---|
|SSSS|Données APP1|Taille des données APP1
|45786966 0000|En-tête Exif
|49492A00 08000000|En-tête TIFF
|XXXX. . . .|IFD0 (image principale)|Répertoire
|LLLLLLLL|Lien vers IFD1
|XXXX. . . .|Zone de données de l'IFD0
|XXXX. . . .|Exif SubIFD|Répertoire
|00000000|Fin du lien
|XXXX. . . .|Zone de données d'Exif SubIFD
|XXXX. . . .|IFD1(image miniature)|Répertoire
|00000000|Fin du lien
|XXXX. . . .|Zone de données de l'IFD1
|FFD8XXXX. . . XXXXFFD9|Vignette

#### En-tête TIFF ####

L'en-tête de fichier [TIFF](/fr/image/tiff/) de 8 octets contient les informations suivantes :

`Octets 0-1 :` L'ordre des octets utilisé dans le fichier. Les valeurs légales sont : « II » (4949.H) « MM » (4D4D.H).

Dans le format « II », l'ordre des octets va toujours de l'octet le moins significatif à l'octet le plus significatif, pour les entiers 16 bits et 32 bits. C'est ce qu'on appelle l'ordre des octets little-endian. Dans le format « MM », l'ordre des octets est toujours du plus significatif au moins significatif, pour les entiers 16 bits et 32 bits. C'est ce qu'on appelle l'ordre des octets gros-boutien.

`Bytes 2-3 :` Un nombre arbitraire mais soigneusement choisi (42) qui identifie davantage le fichier en tant que fichier TIFF. L'ordre des octets dépend de la valeur des octets 0-1.

`Bytes 4-7 :` Le décalage (en octets) du premier IFD. Le répertoire peut se trouver à n'importe quel endroit du fichier après l'en-tête, mais doit commencer sur une limite de mot. En particulier, un répertoire de fichiers d'images peut suivre les données d'image qu'il décrit. Les lecteurs doivent suivre les pointeurs partout où ils peuvent mener. Le terme décalage d'octet est toujours utilisé dans ce document pour désigner un emplacement par rapport au début du fichier TIFF. Le premier octet du fichier a un décalage de 0.

#### Répertoire de fichiers d'images ####

Un IFD contient des informations sur l'image ainsi que des pointeurs vers les données d'image réelles. , suivi d'un décalage de 4 octets du prochain IFD (ou 0 s'il n'y en a pas). Il doit y avoir au moins 1 IFD dans un fichier TIFF et chaque IFD doit avoir au moins une entrée.

##### Entrée IFD #####

Chaque entrée IFD de 12 octets est au format suivant.


|Octets|Description
---|---|
|0-1|Le Tag qui identifie le champ
|2-3|Le type de champ
|4-7|Compte du type indiqué
|8-11|Le décalage de valeur, le décalage de fichier (en octets) de la valeur pour le champ. La valeur doit commencer sur une limite de mot ; le décalage de valeur correspondant sera donc un nombre pair. Ce décalage de fichier peut pointer n'importe où dans le fichier, même après que les données d'image

Un champ TIFF est une entité logique composée d'une balise TIFF et de sa valeur. Ce concept logique est implémenté comme une entrée IFD, plus la valeur réelle si elle ne rentre pas dans la partie valeur/décalage, les 4 derniers octets de l'entrée IFD. Les termes champ TIFF et entrée IFD sont interchangeables dans la plupart des contextes.

#### Vignette ####

Le format Exif contient une vignette de l'image (sauf Ricoh RDC-300Z). Habituellement, il est situé à côté de l'IFD1. Il existe 3 formats pour les vignettes ; Format JPEG (JPEG utilise YCbCr), format RVB TIFF, format YCbCr TIFF.

##### Vignette au format JPEG #####

Si la valeur de Compression(0x0103) Tag dans IFD1 est '6', le format de l'image miniature est JPEG. La plupart des images Exif utilisent le format JPEG pour les vignettes. Dans ce cas, vous pouvez obtenir le décalage de la vignette par la balise JpegIFOffset (0x0201) dans IFD1, la taille de la vignette par la balise JpegIFByteCount (0x0202). Le format de données est le format JPEG ordinaire, commence à 0xFFD8 et se termine par 0xFFD9. Il semble que le format JPEG et une taille de 160x120 pixels soient le format de vignette recommandé pour Exif2.1 ou version ultérieure.

##### Vignette au format TIFF #####

Si la valeur de Compression(0x0103) Tag dans IFD1 est '1', le format d'image miniature n'est pas compressé (appelé image TIFF). Le point de départ des données de vignette est la balise StripOffset(0x0111), la taille de la vignette est la somme de la balise StripByteCounts(0x0117).

## Références ##

* [EXIF - Par Wikipédia](https://en.wikipedia.org/wiki/Exif)
* [Format de fichier EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

