{
  "date" : "2019-10-11",
  "keywords" :[ "bz2 fil", "bz2 filformat", "vad är en bz2 fil", "fil", "bz2 exempel", "bz2 filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - komprimerat filformat",
  "description":"Lär dig veta vad en BZ2-fil och API:er är som kan skapa och öppna BZ2-filer.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Vad är BZ2 fil?

BZ2 är komprimerade filer som genereras med [BZIP2](http://www.bzip.org/) komprimeringsmetoden med öppen källkod, mestadels på UNIX- eller Linux-system. Den används för komprimering av en enda fil och är inte avsedd för arkivering av flera filer. Detta är i motsats till TAR-filformatet på samma plattformar som arkiverar flera filer till en enda fil men utan komprimering. Filer komprimerade som BZ2 kan dekomprimeras med applikationer som [WinZip](https://www.winzip.com/win/en/). BZIP2 använder Run-Length Encoding (RLE) eller [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) komprimeringsalgoritm för att uppnå höga nivåer av komprimering.

## BZ2 filformat

Det finns inga formella specifikationer tillgängliga för detta filformat. En inofficiell [omvänd specifikationer](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) visar dock att en .bz2-ström består av en 4-byte header som följs med noll eller fler komprimerade block. Den följs omedelbart av en strömslutsmarkör som innehåller en 32-bitars CRC för den klartextbearbetade hela strömmen. Det finns ingen stoppning mellan de komprimerade blocken och alla blocken är bitjusterade.

## Packa upp/extrahera BZ2-fil

Du kan packa upp en BZ2-fil på Windows och Mac OS med programvara som WinZip. På linux, följande kommando i terminal.

```
bzip2 -d filename.bz2
```

## Referenser

* [BZIP2-formatspecifikationer](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

