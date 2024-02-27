{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om NSF filformat og API'er, der kan oprette og åbne NSF filer.",
  "title": "NSF-filformat - Lotus Notes-databaseformat",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-daf"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er en NSF fil?

En fil med filtypenavnet .nsf (Notes Storage Facility) er et databasefilformat, der bruges af [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino), som tidligere var kendt som Lotus Notes. Det definerer skemaet til at gemme forskellige slags objekter såsom e-mails, aftaler, dokumenter, formularer og visninger. Alle disse oplysninger er indeholdt i en enkelt NSF-fil til forretningssamarbejde, der ligner en PST/OST-fil. Nogle af de programmer, der kan åbne NSF-filer, inkluderer IBM Lotus Notes og IBM Domino.

## NSF filformatspecifikationer

NSF-filer er binære i naturen, og deres specifikationer er tilgængelige af Joachim Metz på [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). I henhold til disse detaljer består en NSF-fil af:

 * Filoverskrift
 * Databasehoved

Derudover består den af:

 * Superblok
 * Bucket descriptor blok
 * Bitmap
 * Record Relocation Vector spand
 * Opsummering spande
 * Ikke-opsummerende spande


### NSF-filoverskrift

NSF-filheaderen er 6 bytes stor. Den består af:

|Offset|Størrelse|Værdi|Beskrivelse|
---|---|---|---|
0|2|0x1a 0x00|Signatur|
2|4| |Størrelse på databasehovedet|

### Databasehoved

NSD-databasehovedet indeholder følgende bekræftede værdier.

 * Databaseoplysninger
   * Database-id (DBID)
 * Replikationsoplysninger
 * Database information buffer flag
   * Titel
   * Kategorier
   * klasse
   * Designklasse (skabelonnavn)
 * Særlige note identifikatorer
 * Polstring
 * Databaseoplysninger 2
 * Databaseoplysninger 3
 * Databaseoplysninger 4
 * Databaseoplysninger 5
 * Polstring
 * Databaseforekomst-id (DBIID)
 * Replikationshistorie

## Referencer

 * [NSF-format - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

