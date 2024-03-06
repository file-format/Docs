{
  "date": "2021-02-25",
  "keywords": [
"bdf fails",
"bdf faila formāts",
"kas ir bdf fails",
"failu",
"bdf piemērs",
"bdf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF — glifu bitkartes izplatīšanas formāts",
  "description": "Uzziniet par BDF failu formātu un API, kas var izveidot un atvērt BDF failus.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-lvf"
}
},
  "lastmod": "2021-02-25"
}

## Kas ir BDF fails?
BDF faili ir cilvēka lasāmā formā un parasti tiek izplatīti ASCII kodējumā. Fails sākas ar globālo informāciju, kas attiecas uz visu fontu, kam seko informācija un bitkartes atsevišķiem glifiem. Tajā esošie dati tiek rādīti fontam viena izmēra orientācijai. Metrikas, kas jāizmanto vairāk nekā vienā virzienā, var būt ietvertas vienā failā. BDF failā katrs vienums failā atrodas atsevišķā teksta rindiņā. Atstarpes tiek izmantotas, lai atdalītu vienumus rindā.

## BDF faila formāts
BDF šorti Glyph Bitmap Distribution Format; Adobe piederošais faila formāts bitkartes tipa fontu saglabāšanai. Saturs ir teksta fails, kas paredzēts gan datora, gan cilvēka lasīšanai. BDF tiek īpaši izmantots Unix X Window vidēs. Tas ir plaši aizstāts ar PCF fontu formātu, kam vajadzētu būt efektīvākam, un OpenType un TrueType fontiem.
### BDF failu struktūra
BDF fonta fails sastāv no trim sadaļām:

- globāla sadaļa, kas attiecas uz visiem fonta glifiem.
- sadaļa ar atsevišķu ierakstu katram glifam.
- ENDFONT paziņojums.

## Piemērs
Šeit ir fonta piemērs, kurā ir viens glifs ASCII lielajam lielumam A”. Tās globālās deklarācijas sākas ar rindiņu STARTFONT un beidzas ar rindu CHARS.
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



## Atsauces
 * [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glyph Bitmap Distribution Format (BDF) specifikācija](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

