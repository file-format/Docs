{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om LDF-filformat och API:er som kan skapa och öppna LDF-filer.",
  "title" :"LDF - SQL Server Master Database File Format",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är LDF fil?

En fil med filtillägget .ldf är en loggfil som underhålls av Microsoft SQL Server som är ett relationsdatabashanteringssystem (RDBMS). Alla transaktioner som utförs på primära databasfiler ([MDF](/sv/database/mdf/))(såsom infogning, uppdatering, radering) registreras i LDF-filen. LDF-filer är viktiga komponenter i vilken databas som helst. I händelse av ett systemfel används loggfilen för att återställa databasen till ett konsekvent tillstånd. Transaktionsloggfilen kan öka i storlek om transaktionerna inte genomförs fullt ut. LDF-filer kan öppnas med Microsoft SQL Server-programvaran.

## Operationer registrerade i LDF-fil

En SQL-loggfil registrerar följande operationer:

* Början och slutet av varje transaktion.

* Varje datadataändring (infoga, uppdatera eller ta bort). Detta inkluderar även ändringar av systemlagrade procedurer eller DDL-satser (Data Definition Language) till valfri tabell, inklusive systemtabeller.

* Varje omfattning och sida tilldelning eller deallokering.

* Skapa eller släppa en tabell eller index.

## LDF filformat

LDF-filen består av SQL Server-transaktionsposter som är ordnade som en sträng av loggposter. Varje loggpost har ett loggsekvensnummer (LSN) som är högre än LSN för den föregående posten. Strängarna är sammanlänkade efter varandra i filen. På grund av de moderna höghastighetsdatorerna kan poster infogas där LSN2 finns i loggfilen före LSN1. Eftersom operationerna är registrerade i en serie utfördes ändringen som beskrivs av LSN2 efter loggposten LSN1. Posterna för en viss transaktion länkas bakåt med hjälp av pekare som används och påskyndar återställningen av transaktionen.
 

## Referenser

* [Databasfiler och filgrupper](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Transaction Log Architecture and Management Guide](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- server-ver15)

