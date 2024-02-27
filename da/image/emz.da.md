{
  "date": "2019-10-11",
  "keywords": [
"emz fil",
"emz filformat",
"hvad er en emz fil",
"fil",
"emz eksempel",
"emz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMZ-filformat - En Windows-komprimeret forbedret metafil",
  "description": "Lær om EMZ filformat og API'er, der kan oprette og åbne EMZ filer.",
  "linktitle": "EMZ",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-daz"
}
},
  "lastmod": "2020-10-24"
}

## Hvad er en EMZ fil?

En fil med filtypen .emz er en komprimeret beholder af Enhanced Metafile ([EMF](/image/emf/) fil). Disse komprimeres ved hjælp af [GZIP](/compression/gz/)-komprimeringsteknikken, som er den almindeligt anvendte komprimeringsmetode på UNIX- og LINUX-operativsystemer. Fjern linket til ZIP (/compression/zip/), GZIP komprimerer arkivet som helhed i stedet for at komprimere individuelle filer. EMZ-filer er mindre i størrelse sammenlignet med EMF-filer og hjælper med hurtig overførsel under online fildeling. Nogle af de programmer, der kan åbne EMZ-filer, inkluderer Microsoft Visio 2019, Microsoft Office 2019, XnView MP og File Viewer Plus.

## EMZ filformat

EMZ-filer er [Gzip](/compression/gz/) komprimerede og indeholder [EMF](/image/emf/) indeni. Gzip bruger DEFLATE-algoritmen til komprimering af arkivet og er anderledes i anvendelse af komprimering. En EMZ-fil kan dekomprimeres ved at bruge GZip-komprimeringsværktøjer såsom GNU Zip. Filformatet består af:

 * Filoverskrift
 * Valgfri overskrifter
 * Komprimerede data
 * Filsidefod

GZIP-filformatet [specifications version 4.3](https://datatracker.ietf.org/doc/html/rfc1952) udgivet af Internet Engineering Task Force (IETF) indeholder detaljerede oplysninger om filformatet.

## Referencer

 * [RFC1952: GZIP-filformatspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), af [IETF](https://www.ietf.org/)
 * [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

