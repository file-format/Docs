{
  "date" : "2021-08-24",
  "keywords" :[ "trc file", "trc file format", "wat is een trc file", "file", "trc example", "trc file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over TRC-bestandsindeling en API's die TRC-bestanden kunnen maken en openen.",
  "title" :"TRC - SQL Server-traceringsbestand",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Wat is een TRC-bestand?
Een bestand met de extensie .trc bevat de traceerresultaten van de activiteit van een Microsoft SQL-serverdatabase. Deze bestanden worden gemaakt door een software-SQL Server Profiler; meestal verpakt met Microsoft SQL Server-software. De databasebeheerders kunnen een reeks database-instructies analyseren en het traceringslogboek bekijken als er fouten of waarschuwingen worden vermoed. Deze bestanden bevinden zich meestal in de typische LOG-map van MSSQL in de map Program Files op een Windows-besturingssysteem.

## TRC-bestandsindeling
Het TRC-bestandsformaat wordt door SQL Server Profiler gebruikt om automatisch een nieuw spoor te genereren van de recentelijk uitgevoerde instructies door MS SQL-server. De SQL Server Profiler gebruikt de standaardsjabloon voor elke nieuwe tracering. De software bevat echter verschillende vooraf gedefinieerde sjablonen voor het bewaken van bepaalde soorten gebeurtenissen. Ook kan SQL Server Profiler worden gebruikt om sjablonen te maken die de gebeurtenisklassen en gegevenskolommen definiëren die in traceringen moeten worden opgenomen.

### Vooraf gedefinieerde sjablonen
Hier is de lijst met enkele vooraf gedefinieerde sjablonen die zijn opgenomen in SQL Server Profiler:
- **SP_Counts**: registreert het uitvoeringsgedrag van opgeslagen procedures in de loop van de tijd.
- **Standaard**: Generiek startpunt voor het maken van een trace.
- **TSQL**: legt alle Transact-SQL-instructies vast die door clients naar SQL Server worden verzonden en de tijd die is uitgegeven.
- **TSQL_Duration**: legt alle Transact-SQL-instructies vast die door clients naar SQL Server zijn verzonden, hun uitvoeringstijd en groepeert ze op duur.
- **TSQL_Grouped**: gebruik om vragen van een bepaalde klant of gebruiker te onderzoeken.
- **TSQL_Locks**: wordt gebruikt om problemen met deadlocks, time-out voor vergrendelingen en escalatie-gebeurtenissen op te lossen.
- **TSQL_Replay**: gebruik om iteratieve afstemming uit te voeren, zoals benchmarktests.
- **TSQL_SPs**: gebruik om de componentstappen van opgeslagen procedures te analyseren.
- **Tuning**: gebruik om traceeroutput te produceren die Database Engine Tuning Advisor kan gebruiken als werkbelasting om databases af te stemmen.
### Een spoor correleren met gegevens van Windows Performance Log
De SQL Server Profiler kan worden gebruikt om een prestatielogboek van Microsoft Windows te openen, de tellers te kiezen die moeten worden gecorreleerd met een tracering en de geselecteerde prestatiemeteritems naast de tracering weer te geven in de gebruikersinterface van MS SQL Server Profiler. Om de prestatielogboekgegevens aan te geven die correleren met de geselecteerde traceergebeurtenis, wordt een verticale rode balk weergegeven in het gegevensvenster van de systeemmonitor van SQL Server Profiler.


## Referenties ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

