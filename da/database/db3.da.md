{
  "date": "2019-12-12",
  "keywords": [
"DB3",
"DB3 filformat",
"DB3 fil",
"SQLite",
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
  "description": "Lær om DB3-filformat og API'er, der kan oprette og åbne DB3-filer.",
  "title": "DB3 filformat",
  "linktitle": "DB3",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-da3"
}
},
  "lastmod": "2020-11-09"
}

## Hvad er en DB3-fil?
DB3-filen er en databasefil oprettet af SQLite-softwaren, som er et letvægts, selvstændigt databaseprogram, der opretter databaser ved hjælp af almindelige filer; indeholder databasens anatomi samt dataposter; almindeligvis brugt til at hente eller gemme strukturerede data ved hjælp af SQL. Disse filer kan bruges i smarte enheder, eller hvor journalføring eller anden datahåndtering kræves, men i et miljø med lav plads.


## DB3 filformat
DB3-filformatet er forbundet med RDBMS (Relational Database Management System) SQLite, et populært valg til indlejret database. Der er ikke defineret nogen specifik filtypenavn i en SQLite_3 i dens specifikation, den kan bruge udvidelser inklusive [.dbf](/database/dbf/) og [.sqlite](/database/sqlite/).

### Databasesecifikationen
Commonly SQLite, version 3 related db file format can be considered as the DB3 file format used as the publicly documented native format for the SQLite database engine since June 2004. DB3-filformatet er en cross-platform, der kan overføres mellem big-endian og little-endian arkitekturer eller 32-bit og 64-bit systemer. Disse funktioner gør DB3 til et populært valg som applikationsfilformat. Hovedfilen til SQLite_3-databasen (DB3) består af en eller flere sider. Alle størrelser på alle sider er ens i samme database. Sidestørrelsen i bytes er en potens på to mellem 512 og 65536 inklusive.



## Referencer ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)

* [SQLite, version 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)


