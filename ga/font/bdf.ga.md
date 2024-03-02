{
  "date": "2021-02-25",
  "keywords": [
"comhad bdf",
"Formáid comhaid bdf",
"Cad is comhad bdf ann",
"comhad",
"sampla bdf",
"Síneadh comhad bdf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF - Formáid Dáileacháin Glyph Bitmap",
  "description": "Foghlaim faoi fhormáid comhaid BDF agus APIanna ar féidir leo comhaid BDF a chruthú agus a oscailt.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-gaf"
}
},
  "lastmod": "2021-02-25"
}

## Cad is comhad BDF ann?
Is foirm inléite daonna iad comhaid BDF agus dáiltear iad de ghnáth in ionchódú ASCII. Tosaíonn an comhad le faisnéis dhomhanda a bhaineann leis an gcló iomlán, agus ina dhiaidh sin faisnéis agus léarscáileanna giotán do na glyphs aonair. Taispeánann na sonraí ann don chló le haghaidh treoshuíomh aon mhéide. Féadfar an mhéadracht atá le húsáid i níos mó ná treo amháin a chuimsiú in aon chomhad amháin. I gcomhad BDF, tá gach mír ar líne téacs ar leith sa chomhad. Úsáidtear spásanna chun na míreanna a scaradh ar líne.

## Formáid comhaid bDF
The BDF shorts for Glyph Bitmap Distribution Formáid; Is le Adobe é formáid comhaid chun clónna de chineál bitmap a shábháil. Tá an t-ábhar i bhfoirm comhaid téacs atá ceaptha a bheith inléite ag ríomhaire agus ag daoine. Úsáidtear an BDF go háirithe i dtimpeallachtaí Fuinneog Unix X. Tá sé curtha ina áit go forleathan ag an bhformáid chló PCF atá ceaptha a bheith níos éifeachtaí, agus ag clónna OpenType agus TrueType.
### Struchtúr comhaid BDF
Tá trí chuid i gclóchomhad BDF:

- roinn dhomhanda a bhaineann le gach glyph i gcló.
- cuid le hiontráil ar leith do gach glyph.
- ráiteas ENDFONT.

## Sampla
Seo cló samplach ina bhfuil glyph amháin, do phríomhchathair ASCII ‘A’. Tosaíonn a dearbhuithe domhanda leis an líne STARTFONT agus críochnaíonn siad leis an líne CHARS.
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



## Tagairtí
 * [Formáid Dáileacháin Glyph Bitmap](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Sonraíocht Formáid Dáileacháin Glyph Bitmap (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

