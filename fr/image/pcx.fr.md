{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PCX - Fichier d'image bitmap Paintbrush",
  "description":"En savoir plus sur le format de fichier PCX et les API qui peuvent créer et ouvrir des fichiers PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Qu'est-ce qu'un fichier PCX ?

Un fichier PCX, fichier Picture Exchange, est un format de fichier d'image raster utilisé comme format de fichier natif pour l'application PC Paintbrush. Il a été développé par ZSoft Corporation, États-Unis pour les plates-formes DOS et Windows et a été adopté comme principal format de fichier d'imagerie avant l'arrivée de [BMP](/fr/image/bmp/), [JPEG](/fr/image/jpeg/) et [ PNG](/fr/image/png/). Les fichiers PCX sont plus petits car ils sont compressés à l'aide du codage RLE. Il est utilisé dans le fichier multipage [DCX](/fr/image/dcx/) qui sert principalement à créer des fichiers de télécopie numérique.

## Format de fichier PCX

Les fichiers PCX sont enregistrés sur le disque au format de fichier binaire. La structure du format de fichier interne suit l'ordre des octets Little Endian et comporte les trois sections suivantes :

**`En-tête PCX`** - Un en-tête PCX a une longueur de 128 octets. Il contient un identifiant, un numéro de version, les dimensions de l'image, 16 couleurs de palette, le nombre de plans de couleur et la profondeur de bits de chaque plan, ainsi qu'une valeur pour la méthode de compression.

L'en-tête PCX est illustré ci-dessous en référence à l'encyclopédie des formats de fichiers graphiques (2e éd.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Image Data`** - Les données d'image PCX suivent juste après l'en-tête. Les données d'image peuvent être compressées en fonction du réglage de champ dans l'en-tête. Le stockage des données dans le fichier PCX dépend du nombre de plans de couleur spécifiés. Les données d'image sont organisées en lignes. Dans le cas de plusieurs plans, ceux-ci sont stockés par plan dans une rangée dans un arrangement séquentiel de données rouges, vertes et bleues. Ce motif est répété pour chaque ligne du plan.

## Références

* [PCX - Par Wikipédia](https://en.wikipedia.org/wiki/PCX)

