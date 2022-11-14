{
  "date" : "2021-02-25",
  "keywords" :[ "bdf-bestand", "bdf-bestandsformaat", "wat is een bdf-bestand", "bestand", "bdf-voorbeeld", "bdf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Glyph Bitmap-distributieformaat",
  "description":"Meer informatie over BDF-bestandsindelingen en API's die BDF-bestanden kunnen maken en openen.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Wat is een BDF-bestand?
BDF-bestanden zijn voor mensen leesbare vorm en worden meestal gedistribueerd in een ASCII-codering. Het bestand begint met globale informatie die relevant is voor het volledige lettertype, gevolgd door de informatie en bitmaps voor de individuele glyphs. De gegevens daarin worden weergegeven voor het lettertype voor een oriëntatie met één formaat. De metrieken die in meer dan één richting moeten worden gebruikt, kunnen in één bestand zijn opgenomen. In het BDF-bestand staat elk item op een aparte tekstregel in het bestand. Spaties worden gebruikt om de items op een regel te scheiden.

## BDF-bestandsindeling
De BDF-shorts voor Glyph Bitmap Distribution Format; eigendom van Adobe is een bestandsindeling voor het opslaan van lettertypen van het bitmaptype. De inhoud heeft de vorm van een tekstbestand dat bedoeld is om zowel voor de computer als voor mensen leesbaar te zijn. De BDF wordt vooral gebruikt in Unix X Window-omgevingen. Het is op grote schaal vervangen door het PCF-lettertypeformaat, dat efficiënter zou moeten zijn, en door OpenType- en TrueType-lettertypen.
### BDF-bestandsstructuur
Een BDF-lettertypebestand bestaat uit drie secties:

- een algemene sectie die van toepassing is op alle glyphs in een lettertype.
- een sectie met een aparte vermelding voor elke glyph.
- de ENDFONT-verklaring.

## Voorbeeld
Hier is een voorbeeldlettertype met één glyph, voor ASCII-hoofdletter 'A'. De globale declaraties beginnen met de regel "STARTFONT" en eindigen met de regel "CHARS"
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



## Referenties
* [Glyph-bitmapdistributieformaat](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) Specificatie](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

