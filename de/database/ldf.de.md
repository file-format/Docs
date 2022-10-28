{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das LDF-Dateiformat und APIs, die LDF-Dateien erstellen und öffnen können.",
  "title" :"LDF - SQL Server-Master-Datenbankdateiformat",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine LDF-Datei?

Eine Datei mit der Erweiterung .ldf ist eine Protokolldatei, die von Microsoft SQL Server verwaltet wird, einem relationalen Datenbankverwaltungssystem (RDBMS). Alle Transaktionen, die an primären Datenbankdateien ([MDF](/de/database/mdf/)) durchgeführt werden (wie Einfügen, Aktualisieren, Löschen) werden in der LDF-Datei aufgezeichnet. LDF-Dateien sind kritische Komponenten jeder Datenbank. Im Falle eines Systemausfalls wird die Protokolldatei verwendet, um die Datenbank wieder in einen konsistenten Zustand zu versetzen. Die Transaktionsprotokolldatei kann größer werden, wenn Transaktionen nicht vollständig festgeschrieben werden. LDF-Dateien können mit der Microsoft SQL Server-Softwareanwendung geöffnet werden.

## In der LDF-Datei aufgezeichnete Vorgänge

Eine SQL-Protokolldatei zeichnet die folgenden Vorgänge auf:

* Beginn und Ende jeder Transaktion.

* Jede Datenänderung (Einfügen, Aktualisieren oder Löschen). Dazu gehören auch Änderungen durch gespeicherte Systemprozeduren oder DDL-Anweisungen (Data Definition Language) an Tabellen, einschließlich Systemtabellen.

* Jede Extent- und Seitenzuweisung oder -freigabe.

* Erstellen oder Löschen einer Tabelle oder eines Indexes.

## LDF-Dateiformat

Die LDF-Datei besteht aus SQL Server-Transaktionsdatensätzen, die als Zeichenfolge von Protokolldatensätzen angeordnet sind. Jeder Protokolldatensatz hat eine Protokollsequenznummer (LSN), die höher ist als die LSN des vorherigen Datensatzes. Die Strings werden in der Datei hintereinander verkettet. Aufgrund der modernen Hochgeschwindigkeitscomputer können Datensätze eingefügt werden, bei denen die LSN2 in der Protokolldatei vor LSN1 vorhanden ist. Da die Vorgänge seriell aufgezeichnet werden, wurde die durch LSN2 beschriebene Änderung nach dem Protokollsatz LSN1 durchgeführt. Die Aufzeichnungen für eine bestimmte Transaktion werden unter Verwendung von Zeigern, die verwendet werden, rückwärts verknüpft und beschleunigen das Rollback der Transaktion.
 

## Verweise

* [Datenbankdateien und Dateigruppen](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Transaction Log Architecture and Management Guide](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- Server-Version 15)

