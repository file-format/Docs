{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om MDF-filformat och API:er som kan skapa och öppna NDF-filer.",
  "title" :"NDF-filformat - SQL Server Master Database File",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är NDF fil?

En fil med filtillägget .ndf är en sekundär databasfil som används av [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) för att lagra användardata. NDF är en sekundär lagringsfil eftersom SQL-servern lagrar användarspecificerad data i den primära lagringsfilen känd som [MDF](/sv/database/mdf/). NDF-datafilen är valfri och är användardefinierad för att hantera datalagring om den primära MDF-filen använder allt tilldelat utrymme. Det lagras vanligtvis på separat disk och kan spridas till flera lagringsenheter. Förekomsten av MDF-filer är nödvändig för att öppna NDF-filer.

## NDF filformat

NDF-filformat skiljer sig inte från [MDF](/sv/database/mdf/) och använder sidor som den grundläggande enheten för datalagring. varje sida börjar med 96 byte header som inkluderar:

* Sid-ID
* Typ av struktur
* Antal poster på sidorna
* Pekare till föregående och nästa sidor

### NDF-filstruktur

En MDF-fil har följande datastruktur.

* Sida 0: Rubrik
* Sida 1: Första PFS
* Sida 2: Första GAM
* Sida 3: Första SGAM
* Sida 4: Oanvänd
* Sida 5: Oanvänd
* Sida 6: Första DCM
* Sida 7: Första BCM

#### NDF-filhuvud

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

## Datafilsida

Sidor i en SQL Server-datafil börjar från noll (0) och ökar sekventiellt. Varje fil känns igen av ett unikt fil-ID-nummer. Fil-ID och sidnummerpar identifierar unikt en sida i en databas. Ett exempel som visar sidnummer i en databas, är som i följande bild.

{{< figure src="../ndf.png" alt="NDF-databasfilformat" >}}

Det här exemplet visar sidnummer i en databas som har en 4 MB primär datafil och 1 MB sekundär datafil.

## Referenser

* [Databasfiler och filgrupper](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Databas loss and attach - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

