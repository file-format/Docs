{
  "date": "2019-10-11",
  "keywords": [
"mng fil",
"mng filformat",
"hvad er en mng-fil",
"fil",
"mng eksempel",
"mng filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MNG-filformat - Multiple Image Network Graphics-filformat",
  "description": "Lær om MNG-filformat og API'er, der kan oprette og åbne MNG-filer.",
  "linktitle": "MNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-mn-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en MNG fil?

En fil med filtypenavnet .mng er et Multiple-image Network Graphics-filformat, der ligner [PNG](/image/png/) billedformat, men understøtter animerede billeder. Det blev udviklet for at undgå at overbelaste PNG-formatet med yderligere funktioner i animationer. MNG ligner også [GIF](/image/gif/) filer, men bruger mere komprimering og understøtter fuld alfa-funktion. Den uofficielle MIME-medietype for MNG-filer er video/x-mng. MNG-filer kan åbnes i applikationer som ImageMagik og IrfanView.

## MNG filformat

MNG-filformatet ligner det for PNG og bruger den samme chunk-struktur som defineret i PNG-specifikationerne. En MNG-dekoder skal være i stand til at afkode PNG-datastrømmene uden at angive særlige flag for afkodningsinstruktioner. MNG grupperer flere billeder sammen til en ramme, hvor nogle billeder bruges som sprite til at flytte fra et sted til et andet. Mekanismen tillader genbrug af billeddata uden at gentransmittere dem. [MNG specifications](http://www.libpng.org/pub/mng/spec/) kan henvises til for udviklerens reference.

### MNG-signatur

MNG-datastrømmen begynder med en 8-byte signatur, der indeholder:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Dette svarer til PNG-signaturen, men indeholder MNG i stedet for PNG.

### MNG-ramme

En MNG-ramme består af todimensionelle billeder af mindre billeder. Hvert lille billede kan tilgås ved hjælp af række- og kolonneindekskombinationen. Formatet er i stand til at lagre tredimensionelle voxel-data, der er arrangeret en række todimensionelle planer. Hvert plan er repræsenteret af en PNG- eller Delta-PNG-datastrøm. Hver Delta-PNG-datastrøm definerer et billede som forskellene fra det overordnede PNG-billede. Dette giver en meget mere kompakt måde at repræsentere efterfølgende billeder på end at bruge en komplet PNG-datastrøm for hver.

## Referencer ##

* [MNG](http://www.libpng.org/pub/mng/)

* [MNG-format v 1.0](http://www.libpng.org/pub/mng/spec/)


