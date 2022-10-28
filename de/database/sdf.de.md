{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf-Datei", "was ist eine sdf-Datei", "wie man eine sdf-Datei öffnet", "Erweiterung", "Datei", "sdf-Dateiformat", "Datenbankdateityp", "Datenbankdateiformat ", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das SDF-Dateiformat und APIs, die SDF-Dateien erstellen und öffnen können.",
  "title" :"SDF - SQL Server Compact-Datenbankdatei",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Was ist eine SDF-Datei?
Eine Datei mit der Erweiterung .sdf enthält die Microsoft SQL Server Compact (SQL CE)-Datenbank, die auch als kompakte relationale Datenbank bekannt ist; von Microsoft für die Anwendungen entwickelt, die für mobile Geräte und Desktops entwickelt wurden. Es unterstützt sowohl 32- als auch 64-Bit-Betriebssysteme und der vollständige Inhalt der Datenbank ist in einer einzigen SDF-Datei enthalten und kann mehr als 4 GB Speicherplatz belegen. Aus Sicherheitsgründen kann eine .sdf-Datei mit 128-Bit-Verschlüsselung verschlüsselt werden. Die SQL CE-Laufzeit regelt den parallelen Mehrbenutzerzugriff auf die .sdf-Datei. Die SDF-Datei kann über **QuickOnce** kopiert oder einfach an das Ziel für die Systembereitstellung kopiert werden.

## SDF-Dateiformat
Eine SDF-Datei enthält eine Datenbank, die normalerweise als kompakte relationale Datenbank bezeichnet wird. Eine SDF-Datei enthält alle datenbankbezogenen Informationen, und SQL Server Compact ist eine leichte und kostenlose Datenbank-Engine, die zum Verwalten der .sdf-Dateien verwendet wird. Die Größe der .sdf-Datei sollte das Limit von 4 GB nicht überschreiten. Die SDF-Dateien speichern keine Informationen über gespeicherte Prozeduren, Trigger oder Ansichten. Anwendungen, die eine SQL CE-Datenbank verwenden, müssen den Pfad zu einer SDF-Datei nicht in der ADO.NET-Verbindungszeichenfolge angeben, stattdessen kann er als |DataDirectory|\database_name.sdf angegeben werden, wodurch das Datenverzeichnis definiert wird, das im Assemblymanifest für die Anwendung definiert wird
Die Namenskonvention .sdf ist optional, und jede Erweiterung kann zum Speichern der Datei verwendet werden. Das Einrichten eines Kennworts für die Datenbankdatei ist ein optionaler Schritt. Um die Datenbank zu komprimieren oder zu reparieren, sollte die Datei mit der Option **compacted/repaired database** gespeichert werden.

## Verweise

* [SQL Server Compact – Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Verwendung von SQL Server Compact für ASP.NET-Webanwendungen](https://docs.microsoft.com/en-us/ previous-versions/aspnet/ms247257(v=vs.110))


