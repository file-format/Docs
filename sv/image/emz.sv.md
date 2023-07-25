{
  "date" : "2019-10-11",
  "keywords" :[ "emz fil", "emz filformat", "vad är en emz fil", "fil", "emz exempel", "emz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ File Format - En Windows Compressed Enhanced Meta-fil",
  "description":"Läs mer om EMZ-filformat och API:er som kan skapa och öppna EMZ-filer.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Vad är EMZ fil?

En fil med tillägget .emz är en komprimerad behållare med Enhanced Metafile ([EMF](/sv/image/emf/)-fil). Dessa komprimeras med hjälp av komprimeringstekniken [GZIP](/sv/compression/gz/) som är den vanligaste komprimeringsmetoden på UNIX- och LINUX-operativsystem. Ta bort länken till ZIP (/sv/compression/zip/), GZIP komprimerar arkivet som helhet istället för att komprimera enskilda filer. EMZ-filer är mindre i storlek jämfört med EMF-filerna och hjälper till med snabb överföring under online-fildelning. Några av applikationerna som kan öppna EMZ-filer inkluderar Microsoft Visio 2019, Microsoft Office 2019, XnView MP och File Viewer Plus.

## EMZ filformat

EMZ-filer är [Gzip](/sv/compression/gz/) komprimerade och innehåller [EMF](/sv/image/emf/) inuti. Gzip använder DEFLATE-algoritmen för komprimering av arkivet och är annorlunda när det gäller att tillämpa komprimering. En EMZ-fil kan dekomprimeras med hjälp av GZip-komprimeringsverktyg som GNU Zip. Filformatet består av:

* Filhuvud
* Valfria rubriker
* Komprimerad data
* Filsidfot

GZIP-filformatet [specifikationer version 4.3](https://datatracker.ietf.org/doc/html/rfc1952) publicerat av Internet Engineering Task Force (IETF) innehåller detaljerad information om filformatet.

## Referenser

* [RFC1952: GZIP-filformatsspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), av [IETF](https://www.ietf.org/)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

