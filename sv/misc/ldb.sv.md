{
"date": "2023-04-20",
  "keywords": [
"ldb-fil",
"vad är en ldb-fil",
"vilken information ldb innehåller",
"vad är syftet med ldb-fil",
"ldb förlängning",
"fil",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LDB-filformat - Microsoft Access Lock-fil",
  "description":"Läs mer om LDB-format och vilken information det innehåller.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Vad är en LDB fil?

En LDB-fil är en låsfil som används av Microsoft Access för att förhindra att flera användare redigerar samma databas samtidigt. När användaren öppnar en Access-databas skapar Access en motsvarande LDB-fil i samma katalog som databasen. Den här filen innehåller information om vem som för närvarande använder databasen och vilka poster de redigerar.

LDB-filen skapas automatiskt av Microsoft Access när databasen öppnas och tas bort när databasen stängs. Det är viktigt att notera att LDB-filen aldrig bör raderas manuellt eftersom detta kan orsaka problem med databasen.

Om du stöter på problem med Microsoft Access-databasen är en möjlig lösning att försöka ta bort LDB-fil som är associerad med den databasen. Detta släpper alla lås som kan hindra dig från att komma åt databasen. Var dock noga med att göra en säkerhetskopia av databasen innan du försöker detta, eftersom radering av LDB-filen kan orsaka dataförlust eller korruption om den görs felaktigt.

## LDB-filformat - Mer information

En LDB-fil i Microsoft Access innehåller information om användare som för närvarande använder databasen såsom deras användarnamn, datornamn och inloggningstid. LDB-filen innehåller också information om eventuella lås som har placerats på databasen, till exempel vilka poster som redigeras av vilken användare.

Här är en mer detaljerad lista över de typer av information som kan hittas i en LDB-fil:

- **Användarnamn** - namnet på användaren som för närvarande använder databasen
- **Datornamn** - namnet på datorn där användaren kommer åt databasen
- **Inloggningstid** - den tidpunkt då användaren först öppnade databasen
- **Record locks** - information om vilka poster som för närvarande redigeras av vilken användare
- **Objektlås** - information om vilka databasobjekt (som tabeller, formulär eller rapporter) som för närvarande redigeras av vilken användare
- **Anslutningsinformation** - information om hur användaren är ansluten till databasen (till exempel om de använder lokal eller nätverksanslutning)

Informationen i LDB-filen används av Microsoft Access för att förhindra att flera användare gör motstridiga ändringar i samma databas samtidigt. När en användare försöker redigera en post eller ett objekt som redan är låst av en annan användare, kommer Microsoft Access att visa ett meddelande som anger att objektet redan används. LDB-filen uppdateras när användare öppnar och stänger databasen och gör ändringar i låsta objekt.

## Referenser
* [Vad är en LDB-fil?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

