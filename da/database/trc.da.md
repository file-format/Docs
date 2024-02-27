{
  "date": "2021-08-24",
  "keywords": [
"trc filen",
"trc filformat",
"hvad er en trc-fil",
"fil",
"trc eksempel",
"trc filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om TRC filformat og API'er, der kan oprette og åbne TRC filer.",
  "title": "TRC - SQL Server Trace File",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-dac"
}
},
  "lastmod": "2021-08-24"
}

## Hvad er TRC fil?
En fil med filtypenavnet .trc indeholder sporingsresultaterne af aktiviteten i en Miscrosoft SQL-serverdatabase. Disse filer er oprettet af en software SQL Server Profiler; normalt pakket med Microsoft SQL Server-software. Databaseadministratorerne kan analysere en sekvens af databaseudsagn og kan gennemgå sporingsloggen, hvis der er mistanke om en eller anden form for fejl eller advarsler. Disse filer er normalt placeret i den typiske LOG-mappe i MSSQL i mappen Programfiler på et Windows-operativsystem.

## TRC filformat
TRC-filformatet bruges af SQL Server Profiler til automatisk at generere et nyt spor af de nyligt udførte sætninger af MS SQL-serveren. SQL Server Profiler bruger standardskabelonen til enhver ny sporing. Softwaren indeholder dog flere foruddefinerede skabeloner til overvågning af visse typer begivenheder. Også SQL Server Profiler kan bruges til at oprette skabeloner, der definerer de hændelsesklasser og datakolonner, der skal inkluderes i spor.

### Foruddefinerede skabeloner
Her er listen over nogle foruddefinerede skabeloner inkluderet i SQL Server Profiler:
- **SP_Counts**: Fanger opførsel af lagret procedureudførelse over tid.
- **Standard**: Generisk udgangspunkt for at skabe et spor.
- **TSQL**: Indfanger alle Transact-SQL-sætninger, der sendes til SQL Server af klienter, og den udstedte tid.
- **TSQL_Duration**: Indfanger alle Transact-SQL-sætninger sendt til SQL Server af klienter, deres eksekveringstid og grupperer dem efter varighed.
- **TSQL_Grouped**: Bruges til at undersøge forespørgsler fra en bestemt klient eller bruger.
- **TSQL_Låse**: Bruges til at fejlfinde deadlocks, låse timeout og låse eskaleringshændelser.
- **TSQL_Replay**: Bruges til at udføre iterativ tuning, såsom benchmark-test.
- **TSQL_SP'er**: Bruges til at analysere komponenttrinene i lagrede procedurer.
- **Tuning**: Bruges til at producere sporingsoutput, som Database Engine Tuning Advisor kan bruge som en arbejdsbelastning til at tune databaser.
### Korreler et spor med Windows Performance Log-data
SQL Server Profiler kan bruges til at åbne en Microsoft Windows-ydeevnelog, til at vælge de tællere, der skal korreleres med et spor, og vise de valgte ydeevnetællere sammen med sporet i MS SQL Server Profiler GUI. For at angive de præstationslogdata, der korrelerer med den valgte sporingshændelse, skal du bruge en lodret rød bjælke i vinduet System Monitor-data i SQL Server Profiler.


## Referencer ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


