{
  "date": "2019-10-11",
  "keywords": [
"bz2 fil",
"bz2 filformat",
"hvad er en bz2 fil",
"fil",
"bz2 eksempel",
"bz2 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 - komprimeret filformat",
  "description": "Lær at vide, hvad en BZ2-fil og API'er er, der kan oprette og åbne BZ2-filer.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-da2"
}
},
  "lastmod": "2020-09-05"
}

## Hvad er en BZ2 fil?

BZ2 er komprimerede filer genereret ved hjælp af [BZIP2](http://www.bzip.org/) open source-komprimeringsmetoden, for det meste på UNIX- eller Linux-systemer. Det bruges til komprimering af en enkelt fil og er ikke beregnet til arkivering af flere filer. Dette er i modsætning til TAR-filformatet på de samme platforme, der arkiverer flere filer i en enkelt fil, men uden komprimering. Filer komprimeret som BZ2 kan dekomprimeres med applikationer som [WinZip](https://www.winzip.com/win/en/). BZIP2 bruger Run-Length Encoding (RLE) eller [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) komprimeringsalgoritme for at opnå høje niveauer af komprimering.

## BZ2 filformat

Der er ingen formelle specifikationer tilgængelige for dette filformat. Men en uofficiel [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) viser, at en .bz2-strøm består af en 4-byte header, som efterfølges af nul eller flere komprimerede blokke. Den efterfølges umiddelbart af en end-of-stream-markør, der indeholder en 32-bit CRC for hele den behandlede almindelige tekststrøm. Der er ingen polstring mellem de komprimerede blokke, og alle blokkene er bitjusterede.

## Udpak/udpak BZ2-fil

Du kan udpakke en BZ2-fil på Windows og Mac OS ved hjælp af software som WinZip. På linux, følgende kommando i terminal.

```
bzip2 -d filename.bz2
```

## Referencer

* [BZIP2-formatspecifikationer](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


