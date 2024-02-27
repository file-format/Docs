{
  "date": "2021-04-08",
  "keywords": [
"kgb fil",
"kgb filformat",
"hvad er en kgb-fil",
"fil",
"kgb eksempel",
"kgb filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KGB - KGB-arkivfilformat",
  "description": "Lær om KGB-filformat og API'er, der kan oprette og åbne KGB-filer.",
  "linktitle": "KGB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-kg-dab"
}
},
  "lastmod": "2021-04-18"
}

## Hvad er en KGB fil?

En fil med filtypenavnet .kgb er en komprimeret arkivfil, der er oprettet med KGB-arkiveringssoftwaren. KGB-arkiver bruger [PAQ6](https://en.wikipedia.org/wiki/PAQ6)-komprimeringsalgoritmen til at komprimere filerne til et KGB-arkiv. KGB arkiver er udgået og bruges ikke mere. KGB-filformatet tilbyder højere komprimeringshastigheder, men på bekostning af dets minimumshardwarekrav (anbefaler processor med 1,5 GHz ur og 256 MB RAM) og udvidet komprimering/dekompressionstid.

## KGB filformat

Der er ingen tekniske implementeringsdetaljer tilgængelige om KGB-filformatet. Det tilbyder AES-256-kryptering for at beskytte de arkiverede filer. KGB-arkiveringsværktøjet blev udviklet i Visual [C++](/programming/cpp/) af Tomasz Pawlak i april 2006, og det mentes at komprimere en [1 GB file to up to 10 MB](https://web.archive.org/web/20100522074017/http://cshared.com/compress-1-gb-to-10-mb-kgb-archiver/)-fil.

## Referencer

* [KGB - Wikipedia](https://en.wikipedia.org/wiki/KGB_Archiver)

* [KGB Archiver](https://sourceforge.net/projects/kgbarchiver/)


