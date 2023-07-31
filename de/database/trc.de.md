{
  "date" : "2021-08-24",
  "keywords" :[ "trc-Datei", "trc-Dateiformat", "was ist eine trc-Datei", "Datei", "trc-Beispiel", "trc-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das TRC-Dateiformat und APIs, die TRC-Dateien erstellen und öffnen können.",
  "title" :"TRC - SQL Server-Ablaufverfolgungsdatei",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Was ist eine TRC-Datei?
Eine Datei mit der Erweiterung .trc enthält die Ablaufverfolgungsergebnisse der Aktivität einer Miscrosoft SQL Server-Datenbank. Diese Dateien werden von einem Software-SQL Server Profiler erstellt; normalerweise mit Microsoft SQL Server-Software verpackt. Die Datenbankadministratoren können eine Folge von Datenbankanweisungen analysieren und das Ablaufverfolgungsprotokoll überprüfen, wenn Fehler oder Warnungen vermutet werden. Diese Dateien befinden sich normalerweise im typischen LOG-Ordner von MSSQL im Verzeichnis „Programme“ auf einem Windows-Betriebssystem.

## TRC-Dateiformat
Das TRC-Dateiformat wird von SQL Server Profiler verwendet, um automatisch eine neue Ablaufverfolgung der kürzlich ausgeführten Anweisungen von MS SQL Server zu generieren. Der SQL Server Profiler verwendet die Standardvorlage für jede neue Ablaufverfolgung. Die Software enthält jedoch mehrere vordefinierte Vorlagen zur Überwachung bestimmter Arten von Ereignissen. Außerdem kann SQL Server Profiler verwendet werden, um Vorlagen zu erstellen, die die Ereignisklassen und Datenspalten definieren, die in Ablaufverfolgungen eingeschlossen werden sollen.

### Vordefinierte Vorlagen
Hier ist die Liste einiger vordefinierter Vorlagen, die in SQL Server Profiler enthalten sind:
- **SP_Counts**: Erfasst das Ausführungsverhalten von gespeicherten Prozeduren im Laufe der Zeit.
- **Standard**: Allgemeiner Startpunkt zum Erstellen eines Traces.
- **TSQL**: Erfasst alle Transact-SQL-Anweisungen, die von Clients an SQL Server übermittelt werden, sowie die ausgegebene Zeit.
- **TSQL_Duration**: Erfasst alle von Clients an SQL Server übermittelten Transact-SQL-Anweisungen, ihre Ausführungszeit und gruppiert sie nach Dauer.
- **TSQL_Grouped**: Wird verwendet, um Abfragen von einem bestimmten Client oder Benutzer zu untersuchen.
- **TSQL_Locks**: Wird verwendet, um Deadlocks, Sperrzeitüberschreitungen und Sperreskalationsereignisse zu beheben.
- **TSQL_Replay**: Wird verwendet, um iteratives Tuning durchzuführen, wie z. B. Benchmark-Tests.
- **TSQL_SPs**: Wird verwendet, um die Komponentenschritte gespeicherter Prozeduren zu analysieren.
- **Optimierung**: Verwenden Sie diese Option, um Ablaufverfolgungsausgaben zu erstellen, die der Datenbankmodul-Optimierungsratgeber als Arbeitslast zum Optimieren von Datenbanken verwenden kann.
### Eine Ablaufverfolgung mit den Daten des Windows-Leistungsprotokolls korrelieren
Der SQL Server Profiler kann verwendet werden, um ein Microsoft Windows-Leistungsprotokoll zu öffnen, um die mit einer Ablaufverfolgung zu korrelierenden Leistungsindikatoren auszuwählen und die ausgewählten Leistungsindikatoren neben der Ablaufverfolgung in der MS SQL Server Profiler-GUI anzuzeigen. Zeigt die Leistungsprotokolldaten an, die mit dem ausgewählten Ablaufverfolgungsereignis korrelieren, ein vertikaler roter Balken im Datenfensterbereich des Systemmonitors von SQL Server Profiler.


## Verweise ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

