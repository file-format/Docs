{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZIP-filformat - GNU zippad arkivfil",
  "description":"Läs mer om vad en GZIP-fil och API:er är som kan skapa och öppna GZIP-filer.",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## Vad är en GZIP fil?

En GZIP-fil är ett komprimerat arkiv som skapas med standardkomprimeringsalgoritmen [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Det komprimerade arkivet kan innehålla flera filer inklusive komprimerade filer, kataloger och filstubbar. De flesta av Unix-systemen inkluderar komprimeringsverktyget gzip (GNU Zip) med öppen källkod för komprimering/dekomprimering av filer. GZIP-filer kan öppnas med applikationer som [WinZip](https://www.winzip.com/en/).

## GZIP-filformat - Mer information

GZIP använder algoritmen [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) för att komprimera filer till arkiv. Två RFC:er, [RFC1952](https://tools.ietf.org/html/rfc1952) och [RFC 1951](https://tools.ietf.org/html/rfc1951), definierar specifikationerna för gzip-omslagsformatet och tömma komprimerat dataformat, respektive.

GZIP-filer sparas ofta som [GZ](/sv/compression/gz/) filformat.

## Referenser

* [gzip](http://www.gzip.org/)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP filformatspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), av IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

