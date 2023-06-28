{
  "date" : "2019-10-11",
  "keywords" :[ "wmz fil", "wmz filformat", "vad är en wmz fil", "fil", "wmz exempel", "wmz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ-filformat - komprimerad Windows-metafil",
  "description":"Läs mer om WMZ-filformat och API:er som kan skapa och öppna WMZ-filer.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Vad är en WMZ fil?

En fil med filtillägget .wmz är en komprimerad version av [WMF](/sv/image/wmf/) och används för att lagra metafiler. Det är en fil på mellannivå som genereras av äldre versioner av Microsoft Office-program och är inte särskilt populärt. WMZ-filer genereras när dokument sparas i formatet [HTML](/sv/web/html/). Dessa kan också genereras när du skickar dokument med e-post som innehåller inbäddade clipart, ekvationer etc. Program som kan öppna WMZ-filer inkluderar (men inte begränsat till) Corel Winzip och Apple Archive Utility.

## WMZ filformat

WMZ-filer är [Gzip](/sv/compression/gz/) komprimerade och innehåller [WMF](/sv/image/WMF/) inuti. Gzip använder DEFLATE-algoritmen för komprimering av arkivet. GZIP skiljer sig från arkivformatet [ZIP](/sv/compression/zip/) eftersom det tillämpar en komprimeringsalgoritm för att slutföra arkivet snarare än de enskilda filerna. Filformatet består av:

* Filhuvud
* Valfria rubriker
* Komprimerad data
* Filsidfot

GZIP-filformatet [specifikationer version 4.3](http://tools.ietf.org/html/rfc1952) publicerat av Internet Engineering Task Force (IETF) innehåller detaljerad information om filformatet.

## Referenser

* [RFC1952: GZIP filformatspecifikation](http://tools.ietf.org/html/rfc1952), av [IETF](https://www.ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

