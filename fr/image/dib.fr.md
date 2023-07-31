{
  "date" : "2020-01-10",
  "keywords" :[ "fichier dib", "format de fichier dib", "qu'est-ce qu'un fichier dib", "fichier", "exemple dib", "extension de fichier dib","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"En savoir plus sur le format de fichier DIB et les API qui peuvent créer et ouvrir des fichiers DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Qu'est-ce qu'un fichier DIB ?

Un bitmap indépendant du périphérique (DIB) est un fichier d'image raster dont la structure est similaire aux fichiers Bitmap standard ([BMP]()/image/bmp/)). Il contient une table de couleurs qui décrit le mappage des couleurs RVB aux valeurs de pixel. Cela permet à DIB de représenter l'image sur n'importe quel appareil. Il peut être ouvert avec presque toutes les applications capables d'ouvrir un fichier BMP standard sous Windows ainsi que macOS. DIB sont des fichiers binaires et ont un format de fichier complexe similaire à BMP. Les images DIB sont indépendantes des capacités de sortie des appareils de rendu en termes de profondeur de couleur et de pixel par pouce.

## Spécifications du format de fichier DIB ##
Un DIB contient les informations de couleur et de dimension suivantes :

* Le format de couleur de l'appareil sur lequel l'image rectangulaire a été créée.
* La résolution de l'appareil sur lequel l'image rectangulaire a été créée.
* La palette de l'appareil sur lequel l'image a été créée.
* Un tableau de bits qui mappe les triplets rouge, vert, bleu ( RVB ) aux pixels de l'image rectangulaire.
* Un identifiant de compression de données qui indique le schéma de compression de données (le cas échéant) utilisé pour réduire la taille du tableau de bits.

### Format de bloc de données DIB ###

DIB vient dans le contexte du bloc de mémoire par rapport aux fichiers .DIB stockés sur disque. Le bloc de mémoire comprend une structure conforme aux spécifications de l'API Windows pour les DIB. Le DIB réel se compose de :
* Un en-tête
* Palette de couleurs
* Données de pixels

En pratique, travailler avec la palette, l'en-tête et les données d'image se fait comme s'il s'agissait de trois blocs de mémoire distincts. Un descripteur de ce bloc de mémoire commun est attribué à l'aide de GlobalAlloc et est connu sous le nom de HDIB, qui est utilisé pour extraire et travailler avec les données d'en-tête, de table de couleurs et de pixels.

### Ouvrages ###
Les informations contenues dans une DIB sont représentées par différentes structures. Ceux-ci inclus:

BITMAPInfo - Définit les informations de dimension et de couleur pour un DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Il se compose d'un BITMAPINFOHEADER :

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
suivi de deux ou plusieurs structures RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bits de données ###
|Bits|Description|
---|---|
|Format 1 bit (monochrome)|Les bitmaps monochromes se composent de deux couleurs (noir et blanc). En raison de ce nombre limité de couleurs, ces bitmaps occupent moins d'espace sur le disque. Le bitBitCount renvoie true ou false pour la représentation des deux couleurs. La plupart des applications ignorent complètement la palette si bitBitCount==1.
|Format 4 bits (VGA ou 16 couleurs)|Chaque octet de données d'image représente deux pixels et bitBitCount==4. Ces bits représentent la couleur du pixel dans l'ordre décroissant.
|Format 8 bits (256 couleurs)|Ce format 8 bits peut représenter au maximum 256 couleurs. Chaque octet du tableau de données bitmap de l'image représente un seul pixel. La valeur de cet octet est le numéro de l'entrée de la palette de couleurs à utiliser parmi les 256 entrées représentées par bmciColors.
|Format 24 bits (TrueColor)|Ces bitmaps peuvent avoir un maximum de 2^24 couleurs (biBitCount == 24).Chaque séquence de trois octets dans le tableau de données bitmap représente les intensités relatives des trois teintes primaires d'un pixel. Les teintes sont décrites comme des valeurs allant de 0 à 255 et sont stockées dans les trois octets dans l'ordre Bleu, Vert et Rouge. Il s'agit d'une distinction importante, car la plupart des références aux couleurs dans Windows utilisent l'ordre inverse : Rouge/Vert/Bleu, pensez donc "BGR" lorsque vous travaillez avec des images TrueColor au lieu de "RVB". Une palette de couleurs peut être spécifiée pour accélérer le processus de dessin pour Windows, auquel cas biClrUsed ne sera pas 0. Mais comme vous pouvez le voir, ce n'est pas nécessaire, car les données de pixel elles-mêmes contiennent les informations de couleur.
|Format 32 bits|Les images 32 bits ont un maximum de 2^24 couleurs (biBitCount == 24).

## Références ##
* [Bitmaps indépendants de l'appareil - Par Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

