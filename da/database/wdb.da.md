{
  "date": "2021-08-24",
  "keywords": [
"wdb fil",
"wdb filformat",
"hvad er en wdb-fil",
"fil",
"wdb eksempel",
"wdb filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WDB-filformat og API'er, der kan oprette og åbne WDB-filer.",
  "title": "WDB - SQL Server Trace File",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-dab"
}
},
  "lastmod": "2021-08-24"
}

## Hvad er WDB fil?
En fil med filtypenavnet .wdb er faktisk en databasefil oprettet af Microsoft Works, som blev brugt til at udføre funktioner som et databasestyringssystem. WDB-filen ligner Access Database-filen ([MDB](/database/mdb/)), men mindre effektiv og større begrænsninger. WDB-filerne kan ikke åbnes ved hjælp af Microsoft Access. Du kan dog åbne WDB-filen i Microsoft Works og derefter eksportere den til MDB-fil, for at åbne en WDB-fil i MS Access.

## WDB filformat
Microsoft Works Database er det oprindelige databaseformat i Microsoft Works kontorpakken. På grund af formatets proprietære karakter og nogle begrænsninger. WDB-filerne kan ikke åbnes i anden software end Microsoft Works. I filformatet kan en tilbagevendende, 10 byte header findes før hver af ASCII-tekststrengene, der repræsenterer værdierne af felterne, som blev afsluttet med en NULL-værdi. Headeren starter generelt med en **\x0f** byte og NULL, efterfulgt af 4 databytes alterneret med NULL.

### Filstruktur

Strukturen af WDB-filen er angivet nedenfor:
- **1st header**: fra begyndelsen af filen, slutter med \x25\x00\xf2 og 244 NULL bytes
- **2. overskrift**: begynder med \xffT - dvs. \xff\x54 og strækker sig over 4096 bytes, der indeholder kolonne-/feltnavne og andre ting, og ser ud til at begynde ved byteposition 6144.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. databyte 2 er feltnummeret, databyte 3 er postnummeret (tilføjer databyte 3, del 2, når det går over 256 poster).


## Referencer ##

* [Bruger:JesseW/wdb-format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


