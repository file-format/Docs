{
  "date": "2021-02-25",
  "keywords": [
"bdf fil",
"bdf filformat",
"hvad er en bdf-fil",
"fil",
"bdf eksempel",
"bdf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF - Glyph Bitmap Distribution Format",
  "description": "Lær om BDF-filformat og API'er, der kan oprette og åbne BDF-filer.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-daf"
}
},
  "lastmod": "2021-02-25"
}

## Hvad er en BDF fil?
BDF-filer er mennesker, der kan læses og distribueres normalt i en ASCII-kodning. Filen starter med global information, der er relevant for den komplette skrifttype, efterfulgt af information og bitmaps for de enkeltes glyffer. Dataene i den viser for skrifttypen for en enkelt størrelsesorientering. De metrikker, der skal bruges i mere end én retning, kan være omfattet af en enkelt fil. I BDF-filen er hvert element indeholdt på en separat tekstlinje i filen. Mellemrum bruges til at adskille elementerne på en linje.

## BDF filformat
BDF-shortsene til Glyph Bitmap Distribution Format; ejet af Adobe er et filformat til lagring af skrifttyper af bitmap-type. Indholdet har form af en tekstfil, der er beregnet til at være computerlæselig såvel som mennesker. BDF'en bruges især i Unix X Window-miljøer. Det er i vid udstrækning blevet erstattet af PCF-skrifttypeformatet, som formodes at være mere effektivt, og af OpenType- og TrueType-skrifttyper.
### BDF-filstruktur
En BDF-skrifttypefil består af tre sektioner:

- en global sektion, der gælder for alle glyffer i en skrifttype.
- et afsnit med en separat post for hver glyf.
- ENDFONT-erklæringen.

## Eksempel
Her er et eksempel på en skrifttype, der indeholder én glyf, for ASCII stort 'A'. Dens globale erklæringer starter med STARTFONT-linjen og slutter med CHARS-linjen
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



## Referencer
 * [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glyph Bitmap Distribution Format (BDF) Specifikation](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

