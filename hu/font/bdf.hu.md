{
  "date" : "2021-02-25",
  "keywords" :[ "bdf fájl", "bdf fájlformátum", "mi az a bdf fájl", "fájl", "bdf példa", "bdf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Glyph Bitmap Distribution Format",
  "description":"További információ a BDF fájlformátumról és az API-król, amelyek BDF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Mi az a BDF fájl?
A BDF fájlok ember által olvasható formátumúak, és általában ASCII kódolásban terjesztik. A fájl a teljes betűtípusra vonatkozó globális információkkal kezdődik, majd az egyes karakterjelekhez tartozó információkkal és bittérképekkel kezdődik. A benne lévő adatok a betűtípusra vonatkoznak, egyetlen méretű tájoláshoz. Az egynél több irányban használható metrikák egyetlen fájlban is szerepelhetnek. A BDF fájlban minden elem külön szövegsorban található a fájlban. A szóközök a sorban lévő elemek elválasztására szolgálnak.

## BDF fájl formátum
A BDF rövidnadrág a Glyph Bitmap Distribution Format számára; Az Adobe tulajdonában lévő fájlformátum bitmap típusú betűtípusok mentésére. A tartalom számítógépes és ember által olvasható szövegfájl formájában jelenik meg. A BDF-et különösen Unix X Window környezetben használják. Ezt széles körben felváltotta a hatékonyabbnak vélt PCF betűtípus, valamint az OpenType és TrueType betűtípusok.
### BDF fájlszerkezet
A BDF betűtípusfájl három részből áll:

- egy globális szakasz, amely egy betűtípus összes karakterjelére vonatkozik.
- minden karakterjelhez külön bejegyzést tartalmazó szakasz.
- az ENDFONT nyilatkozat.

## Példa
Íme egy példa betűtípusra, amely egy karakterjelet tartalmaz az ASCII nagybetűs „A” számára. Globális deklarációi a "STARTFONT" sorral kezdődnek, és a "CHARS" sorral végződnek
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



## Hivatkozások
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) specifikáció](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

