{
  "date" : "2021-02-25",
  "keywords" :[ "soubor bdf", "formát souboru bdf", "co je soubor bdf", "soubor", "příklad bdf", "přípona souboru bdf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Formát distribuce bitmapy glyfů",
  "description":"Další informace o formátu souborů BDF a rozhraních API, která mohou vytvářet a otevírat soubory BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Co je soubor BDF?
Soubory BDF jsou člověkem čitelné formy a obvykle distribuovány v kódování ASCII. Soubor začíná globálními informacemi relevantními pro celé písmo, po nichž následují informace a bitmapy pro jednotlivé glyfy. Data v něm se zobrazují pro písmo pro orientaci jedné velikosti. Metriky pro použití ve více než jednom směru mohou být zahrnuty v jediném souboru. V souboru BDF je každá položka obsažena na samostatném řádku textu v souboru. Mezery se používají k oddělení položek na řádku.

## formát souboru BDF
BDF šortky pro Glyph Bitmap Distribution Format; vlastněný společností Adobe je formát souboru pro ukládání písem bitmapového typu. Obsah má formu textového souboru, který má být čitelný pro počítač i pro člověka. BDF se používá zejména v prostředí Unix X Window. Byl široce nahrazen formátem písem PCF, který má být efektivnější, a písmy OpenType a TrueType.
### Struktura souborů BDF
Soubor písem BDF se skládá ze tří částí:

- globální sekce, která se vztahuje na všechny glyfy v písmu.
- oddíl se samostatným záznamem pro každý glyf.
- příkaz ENDFONT.

## Příklad
Zde je příklad písma obsahujícího jeden glyf pro ASCII velké 'A'. Jeho globální deklarace začínají řádkem „STARTFONT“ a končí řádkem „CHARS“.
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



## Reference
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Specifikace Glyph Bitmap Distribution Format (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

