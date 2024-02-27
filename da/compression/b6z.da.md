{
  "date": "2019-10-11",
  "keywords": [
"b6z fil",
"b6z filformat",
"hvad er en b6z fil",
"fil",
"b6z eksempel",
"b6z filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "B6Z - B6ZIP arkivfilformat",
  "description": "Lær om B6Z-filformat og API'er, der kan oprette og åbne B6Z-filer.",
  "linktitle": "B6Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-b6-daz"
}
},
  "lastmod": "2021-04-05"
}

## Hvad er en B6Z fil?

En fil med filtypenavnet .b6z er en komprimeret arkivfil oprettet macOS-softwareapplikation [B6Zip](http://b6zip.com), der bruges til at komprimere og dekomprimere filer. Det er et forholdsvis nyt arkivformat, der tillader højere kompressionsforhold. B6Z har åben arkitektur og understøtter filstørrelser op til 900000 PB. Det understøtter datakomprimering, fejlgendannelse og filspænding. B6Zip-hjælpesoftwaren er tilgængelig gratis på MacOS for at åbne forskellige typer komprimerede filer, inklusive B6Z.

## B6Z filformat

B6Z-filformatet er baseret på åben arkitektur og giver solid komprimering med AES-256 krypteringsalgoritme. Den bruger LZMA2 som standard komprimeringsmetode, men understøtter også andre komprimeringsmetoder som følger.

|Metode|Beskrivelse|
---|---|
|LZMA |Optimeret version af LZ77-algoritmen|
|LZMA2| Forbedret version af LZMA|
|Deflatere| Almindelig LZ77-algoritme|
|BZip2| Standard BWT-algoritme|
|PPMD| Dmitry Shkarins PPMdH|

B6Zip-værktøjet understøtter alle disse kompressionsstandarder og er meget optimeret, hvilket resulterer i høj hastighed. Det understøtter arbejde med filformaterne [ZIP](/compression/zip/), [TAR](/compression/tar/) og [RAR](/compression/rar/). B6Z-filer har MIME-typen application/x-b6z-komprimeret.

## Referencer

* [B6Zip](http://b6zip.com)


