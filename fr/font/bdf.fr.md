{
  "date" : "2021-02-25",
  "keywords" :[ "fichier bdf", "format de fichier bdf", "qu'est-ce qu'un fichier bdf", "fichier", "exemple bdf", "extension de fichier bdf","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Format de distribution de bitmap de glyphe",
  "description":"En savoir plus sur le format de fichier BDF et les API qui peuvent créer et ouvrir des fichiers BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Qu'est-ce qu'un fichier BDF ?
Les fichiers BDF sont sous une forme lisible par l'homme et généralement distribués dans un codage ASCII. Le fichier commence par des informations globales relatives à la police complète, suivies des informations et des bitmaps pour les glyphes individuels. Les données qu'il contient s'affichent pour la police pour une orientation de taille unique. Les métriques à utiliser dans plus d'une direction peuvent être comprises dans un seul fichier. Dans le fichier BDF, chaque élément est contenu sur une ligne de texte distincte dans le fichier. Les espaces sont utilisés pour séparer les éléments sur une ligne.

## Format de fichier BDF
Le short BDF pour Glyph Bitmap Distribution Format; appartenant à Adobe est un format de fichier permettant d'enregistrer des polices de type bitmap. Le contenu prend la forme d'un fichier texte destiné à être lisible par ordinateur et par l'homme. Le BDF est particulièrement utilisé dans les environnements Unix X Window. Il a été largement remplacé par le format de police PCF censé être plus efficace, et par les polices OpenType et TrueType.
### Structure du fichier BDF
Un fichier de police BDF se compose de trois sections :

- une section globale qui s'applique à tous les glyphes d'une police.
- une section avec une entrée séparée pour chaque glyphe.
- l'instruction ENDFONT.

## Exemple
Voici un exemple de police contenant un glyphe, pour 'A' majuscule ASCII. Ses déclarations globales commencent par la ligne "STARTFONT" et se terminent par la ligne "CHARS"
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Références
* [Format de distribution de bitmap de glyphe] (https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Spécification du format de distribution Glyph Bitmap (BDF)] (https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

