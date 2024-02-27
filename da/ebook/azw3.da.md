{
  "date": "2019-12-12",
  "keywords": [
"KF8",
"udvidelse",
"fil",
"format",
"e-bog",
"Kindle filformat",
"AZW3 filstruktur"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AZW3-filformat og API'er, der kan oprette og åbne AZW3-filer.",
  "title": "Hvad er en AZW3 fil?",
  "linktitle": "AZW3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-azw-da3"
}
},
  "lastmod": "2021-06-04"
}

## Hvad er en AZW3 fil?

AZW3, også kendt som Kindle Format 8 (**KF8**), er den modificerede version af [AZW](/ebook/azw/) e-bogs digitale filformat udviklet til Amazon Kindle-enheder. Formatet er en forbedring af ældre AZW-filer og bruges kun på Kindle Fire-enheder med bagudkompatibilitet for forfader-filformatet, dvs. [MOBI](/ebook/mobi/) og AZW. Amazon introducerede KFX (KF version 10) format efter KF8, der bruges på de nyeste Kindle-enheder. AZW3-filer har internetmedietypen application/vnd.amazon.mobi8-ebook. AZW3-filer kan konverteres til en række andre filformater såsom [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/) og [RTF](/word-processing/rtf/).

## AZ3/KF8 filformat ##

KF8-filer er binære i naturen og bevarer strukturen af et MOBI-filformat som PDB-fil. Som tidligere nævnt kan en KF8-fil bestå af både en MOBI samt en nyere KF8-version af EPUB senere. De interne detaljer i formatet er blevet afkodet af [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), som er et Python-script, der analyserer den endelige kompilerede database og udtrækker MOBI- eller AZW-kildefiler fra den. AZW3 (KF8)-filer målretter mod EPUB3-version med bagudkompatibilitet for EPUB. KF8 kompilerer EPUB-filerne og genererer en binær struktur baseret på PDB-filformatet.

## Referencer ##

* [KF8 - Af Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)

* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)


