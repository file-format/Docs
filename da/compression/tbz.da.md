{
  "date": "2019-10-11",
  "keywords": [
"tbz filen",
"tbz filformat",
"hvad er en tbz-fil",
"fil",
"tbz eksempel",
"tbz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TBZ - Bzip Compressed Tar Archive",
  "description": "Lær om TBZ filformat og API'er, der kan oprette og åbne TBZ filer.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tb-daz"
}
},
  "lastmod": "2021-04-05"
}

## Hvad er TBZ fil?

En fil med filtypen .tbz er et komprimeret arkiv, der bruger BZIP-komprimering til at reducere størrelsen af indholdsfilerne. TBZ-filerne er faktisk UNIX [TAR](/compression/tar/) arkiverede filer, som derefter komprimeres med BZIP. Den seneste komprimering på andet niveau er [BZIP2](/compression/bz2/), der erstattede BZIP. TBZ filformat er velegnet til overførsel af store filer. TBZ-filer kan åbnes/udpakkes ved hjælp af softwareprogrammer som 7-Zip, PeaZip og jZip. Linux- og macOS-brugere kan også åbne en TBZ med BZIP2-kommandoen fra et terminalvindue.

## TBZ filformat

TBZ-filer er faktisk komprimerede arkiver oprettet med BZIP/[BZIP2](/compression/bz2/)-komprimering. Der er ingen formelle specifikationer tilgængelige for dette filformat. En uofficiel [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) viser dog, at en .bz2-strøm består af en 4-byte header, som efterfølges af nul eller flere komprimerede blokke.

## Referencer ##

* [BZIP2-formatspecifikationer](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


