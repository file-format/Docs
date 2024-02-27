{
  "date": "2021-09-06",
  "keywords": [
"btr",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Btrieve-database"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om BTR filformat og API'er, der kan oprette og åbne BTR filer.",
  "title": "BTR - Btrieve Database File",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bt-dar"
}
},
  "lastmod": "2021-09-06"
}

## Hvad er en BTR fil?

En fil med filtypenavnet .btr er en databasefil oprettet af [Btrieve](https://www.actian.com/) transaktionsdatabaseapplikation. I modsætning til relationelle databasestyringssystemer (RBMS) er Btrieve baseret på indekseret sekventiel adgangsmetode (ISAM), som er en måde at gemme data til hurtig genfinding. BTR-filen gemmer en samling af poster og bruges til at generere rapporter i henhold til kravene. BTR-filer kan åbnes ved hjælp af Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility og Legend Software BTRIEVE Viewer.

## BTR-filstruktur - flere oplysninger

Den interne datastruktur og justering af hver byte i strukturen af en BTR-fil er ikke offentligt tilgængelig. Dog Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * GNU C/C++
 * Micro Focus COBOL
 * Microsoft Visual Basic
 * Microsoft Visual C++
 * Watcom C/C++

Hentning af data fra en BTR-fil er afhængig af den tilhørende DDF-fil. Uden DDF vil det ikke være nemt at hente informationen fra sådan en fil.

## Referencer

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

