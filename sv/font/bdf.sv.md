{
  "date" : "2021-02-25",
  "keywords" :[ "bdf-fil", "bdf-filformat", "vad är en bdf-fil", "fil", "bdf-exempel", "bdf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Glyph Bitmap Distribution Format",
  "description":"Läs mer om BDF-filformat och API:er som kan skapa och öppna BDF-filer.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Vad är en BDF fil?
BDF-filer är läsbara av människor och distribueras vanligtvis i en ASCII-kodning. Filen börjar med global information som är relevant för hela teckensnittet, följt av informationen och bitmappar för individens glyfer. Data i den visas för teckensnittet för en orientering i en storlek. Måtten som ska användas i mer än en riktning kan ingå i en enda fil. I BDF-filen finns varje objekt på en separat textrad i filen. Mellanslag används för att separera objekten på en rad.

## BDF filformat
BDF-shortsarna för Glyph Bitmap Distribution Format; som ägs av Adobe är ett filformat för att spara teckensnitt av bitmappstyp. Innehållet har formen av en textfil som är avsedd att vara läsbar för både datorer och människor. BDF används särskilt i Unix X Window-miljöer. Det har i stor utsträckning ersatts av PCF-teckensnittsformatet som ska vara mer effektivt, och av OpenType och TrueType-teckensnitt.
### BDF-filstruktur
En BDF-teckensnittsfil består av tre sektioner:

- en global sektion som gäller alla glyfer i ett teckensnitt.
- en sektion med en separat post för varje glyf.
- ENDFONT uttalandet.

## Exempel
Här är ett exempel på teckensnitt som innehåller en glyf, för ASCII versalt "A". Dess globala deklarationer börjar med raden "STARTFONT" och slutar med raden "CHARS".
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



## Referenser
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) Specification](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

