{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"udvidelse",
"fil",
"format",
"billede",
"Apple-ikonbillede",
"macOS",
"Æble",
"Ikon"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS - Apple-ikonbillede",
  "description": "Lær om ICNS-filformat og API'er, der kan oprette og åbne ICNS-filer.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-das"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er en ICNS fil? ##

Et ikonformat, der bruges af macOS-programmer, kaldes en ICNS-fil. Den tillader 1-bit og 8-bit alfabånd og gemmer et eller flere billeder, normalt lavet af [PNG](/image/png/) dokumenter. Programikonet i macOS-browseren og grænsefladen vises ved hjælp af ICNS-filer.

Baseret på placeringen kan det samme stilikon have flere indstillinger. ICNS-formatet har gennemgået adskillige ændringer og har udviklet sig til det punkt, hvor det nu kan bruges som grundlag for forskellige kompatible formater. Her er nogle andre vigtige punkter, du skal vide:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource og Mac OS icons Resource er nogle af de andre navne. 

* Til ikonoplysninger bruges en kilde i ressourcegrenen.

* I de fleste tilfælde indeholder en fil adskillige billeder. 1612 pixels kvadrat og 1024, 512, 256, 128, 48, 32 og 16 pixels kvadrat er understøttede billedstørrelser.



## ICNS filformat ##

ICNS-dataformatet er en kapsel til et eller flere billeder, der understøtter 1-bit-bånd og adskillige billedtilstande.
Operativsystemet kan ændre størrelsen på ikonbilleder, så de passer til den ønskede skærmstørrelse. De større ikonbilleder gemmes typisk som [JPEG](/image/jpeg/) 2000 eller [PNG](/image/png/) filer. En type af både komprimerede og ukomprimerede ICNS-filer er mulig.

En header og binære ikondata udgør strukturen af en ICNS-fil. Headeren indeholder 8 bytes data, hvoraf fire er magiske bogstaver, og fire af dem er filens længde. Typen og størrelsen af hvert ikonbillede gemmes i ikondatasektionen, som efterfølges af de binære billeddata. Billedstørrelsen bestemmer den binære sektions størrelse.

## Teknisk specifikation ##

### Header ###

|Offset|Størrelse|Mål
---|---|---|
|0|4|Magisk bogstavelig, skal være icns (0x69, 0x63, 0x6e, 0x73)
|4|4|Længde af fil, i bytes, msb først


### Ikondata ###

|Offset|Størrelse|Mål
---|---|---|
|0|4|Ikontype
|4|4|Længde af data, i bytes (inklusive type og længde), msb først
|8|Variabel|Ikondata

### Kompression ###

Pixeldataene komprimeres til en vis grad. 32-bit (is32, il32, ih32, it32) og ARGB (ic04, ic05) pixels komprimeres ofte (pr. kanal) på samme måde som PackBits.

|Lead Value|Tail Bytes|Resultat (ukomprimeret)
---|---|---|
|0 - 127|1 - 128|1 - 128 bytes
|128 - 255|1 Byte|3 - 130 kopier

## Reference ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


