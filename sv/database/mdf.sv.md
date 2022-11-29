{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om MDF-filformat och API:er som kan skapa och öppna MDF-filer.",
  "title" :"MDF-filformat - SQL Server Master Database File",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är en MDF fil?

En fil med filtillägget .mdf är en masterdatabasfil som används av [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) för att lagra användardata. Det är av största vikt eftersom all data lagras i denna fil. MDF-filen lagrar användardata i relationsdatabaser i formulärkolumner, rader, fält, index, vyer och tabeller. SQL Server gör det möjligt att ställa in inställningar för autogrow och autoshrink för att ha en positiv inverkan på databasens prestanda. MDF-filer kan laddas och bifogas till en databas med hjälp av Microsoft SQL Server. MDF-filer har Application/octet-stream mime-typ.

## MDF filformat

Den grundläggande enheten för datalagring i SQL Server är en sida. En databastilldelad lagringssida är uppdelad i logiska sidor med numrering från 0 till n. En enskild sida börjar med en 96 byte rubrik som består av sid-ID, typ av struktur som sidan tillhör, antal poster på sidan och pekare till föregående och nästa sida.

### Filstruktur

En MDF-fil har följande datastruktur.

* Sida 0: Rubrik
* Sida 1: Första PFS
* Sida 2: Första GAM
* Sida 3: Första SGAM
* Sida 4: Oanvänd
* Sida 5: Oanvänd
* Sida 6: Första DCM
* Sida 7: Första BCM

#### Filhuvud

Sidnummer 0 i alla filer innehåller en rubrik som lagrar metadata om filen.

#### Page Free Space (PFS)
PFS identifierar tilldelningsstatus och bestämmer mängden ledigt utrymme.

* Bit 1: Indikerar om sidan är allokerad eller inte.
* Bit 2: Indikerar om sidan är från en blandad omfattning.
* Bit 3: Indikerar att denna sida är en IAM-sida.
* Bit 4: Indikerar att den här sidan innehåller spökposter
* Bitar 5 till 7: Ett kombinerat tre-bitars värde, som indikerar sidfullheten enligt följande:
* 0: Sidan är tom
* 1: Sidan är 1–50 % full
* 2: Sidan är 51–80 % full
* 3: Sidan är 81–95 % full
* 4: Sidan är 96–100 % full

## Referenser

* [Databasfiler och filgrupper](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Databas loss and attach - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

