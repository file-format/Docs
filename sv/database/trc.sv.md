{
  "date" : "2021-08-24",
  "keywords" :[ "trc-fil", "trc-filformat", "vad är en trc-fil", "fil", "trc-exempel", "trc-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om TRC-filformat och API:er som kan skapa och öppna TRC-filer.",
  "title" :"TRC - SQL Server Trace File",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Vad är TRC fil?
En fil med filtillägget .trc innehåller spårningsresultaten av aktiviteten hos en Miscrosoft SQL-serverdatabas. Dessa filer skapas av en programvara SQL Server Profiler; vanligtvis förpackad med Microsoft SQL Server-programvara. Databasadministratörerna kan analysera en sekvens av databassatser och kan granska spårningsloggen om någon typ av fel eller varningar misstänks. Dessa filer finns vanligtvis i den typiska LOG-mappen i MSSQL i Program Files-katalogen på ett Windows-operativsystem.

## TRC filformat
TRC-filformatet används av SQL Server Profiler för att automatiskt generera ett nytt spår av de nyligen körda satserna av MS SQL-servern. SQL Server Profiler använder standardmallen för alla nya spår. Programvaran innehåller dock flera fördefinierade mallar för övervakning av vissa typer av händelser. Även SQL Server Profiler kan användas för att skapa mallar som definierar händelseklasser och datakolumner som ska inkluderas i spår.

### Fördefinierade mallar
Här är listan över några fördefinierade mallar som ingår i SQL Server Profiler:
- **SP_Counts**: Fångar exekveringsbeteendet för lagrad procedur över tid.
- **Standard**: Generisk utgångspunkt för att skapa ett spår.
- **TSQL**: Fångar alla Transact-SQL-satser som skickas till SQL Server av klienter och den tid som utfärdats.
- **TSQL_Duration**: Fångar alla Transact-SQL-satser som skickas till SQL Server av klienter, deras exekveringstid och grupperar dem efter varaktighet.
- **TSQL_Grouped**: Används för att undersöka frågor från en viss klient eller användare.
- **TSQL_Lås**: Används för att felsöka blockerat låsläge, låsa timeout och låsa eskaleringshändelser.
- **TSQL_Replay**: Används för att utföra iterativ inställning, såsom benchmarktestning.
- **TSQL_SPs**: Används för att analysera komponentstegen i lagrade procedurer.
- **Tuning**: Används för att producera spårningsutdata som Database Engine Tuning Advisor kan använda som en arbetsbelastning för att finjustera databaser.
### Korrelera ett spår med Windows Performance Log-data
SQL Server Profiler kan användas för att öppna en Microsoft Windows prestandalogg, för att välja de räknare som ska korrelera med en spårning och visa de valda prestandaräknare bredvid spåret i MS SQL Server Profiler GUI. För att indikera prestandaloggdata som korrelerar med den valda spårningshändelsen, en vertikal röd stapel i systemövervakarens datafönster i SQL Server Profiler.


## Referenser ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

