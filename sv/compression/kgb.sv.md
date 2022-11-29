{
  "date" : "2021-04-08",
  "keywords" :[ "kgb-fil", "kgb-filformat", "vad är en kgb-fil", "fil", "kgb-exempel", "kgb-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KGB - KGB Archive File Format",
  "description":"Läs mer om KGB-filformat och API:er som kan skapa och öppna KGB-filer.",
  "linktitle" : "KGB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Vad är en KGB fil?

En fil med tillägget .kgb är en komprimerad arkivfil som skapats med KGB-arkiveringsmjukvaran. KGB-arkiveraren använder komprimeringsalgoritmen [PAQ6](https://en.wikipedia.org/wiki/PAQ6) för att komprimera filerna till ett KGB-arkiv. KGB-arkivet har upphört och används inte längre. KGB-filformat erbjuder högre komprimeringshastigheter men till priset av dess lägsta hårdvarukrav (rekommenderar processor med 1,5 GHz klocka och 256 MB RAM) och utökad komprimering/dekompressionstid.

## KGB filformat

Det finns inga tekniska implementeringsdetaljer tillgängliga om KGB-filformatet. Den erbjuder AES-256-kryptering för att skydda de arkiverade filerna. KGB-arkivet utvecklades i Visual [C++](/sv/programming/cpp) av Tomasz Pawlak i april 2006 och det antogs komprimera en [1 GB-fil till upp till 10 MB](https://web.archive.org/ web/20100522074017/http://cshared.com/compress-1-gb-to-10-mb-kgb-archiver/) fil.

## Referenser

* [KGB - Wikipedia](https://en.wikipedia.org/wiki/KGB_Archiver)
* [KGB Archiver](https://sourceforge.net/projects/kgbarchiver/)

