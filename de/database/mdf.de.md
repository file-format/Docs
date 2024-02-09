{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MDF-Dateiformat und APIs, die MDF-Dateien erstellen und öffnen können.",
  "title" :"MDF-Dateiformat - SQL Server-Master-Datenbankdatei",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine MDF-Datei?

Eine Datei mit der Erweiterung .mdf ist eine Master-Datenbankdatei, die von [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) zum Speichern von Benutzerdaten verwendet wird. Es ist von größter Bedeutung, da alle Daten in dieser Datei gespeichert werden. Die MDF-Datei speichert Benutzerdaten in relationalen Datenbanken in Form von Spalten, Zeilen, Feldern, Indizes, Ansichten und Tabellen. SQL Server ermöglicht das Festlegen von Autogrow- und Autoshrink-Einstellungen, um sich positiv auf die Leistung der Datenbank auszuwirken. MDF-Dateien können mit Microsoft SQL Server geladen und an eine Datenbank angehängt werden. MDF-Dateien haben den MIME-Typ Application/octet-stream.

## MDF-Dateiformat

Die grundlegende Einheit der Datenspeicherung in SQL Server ist eine Seite. Eine von der Datenbank zugewiesene Speicherseite ist in logische Seiten unterteilt, die von 0 bis n nummeriert sind. Eine einzelne Seite beginnt mit einem 96-Byte-Header, der die Seiten-ID, den Strukturtyp, zu dem die Seite gehört, die Anzahl der Datensätze auf der Seite und Zeiger auf die vorherige und nächste Seite umfasst.

### Dateistruktur

Eine MDF-Datei hat die folgende Datenstruktur.

* Seite 0: Kopfzeile
* Seite 1: Erstes PFS
* Seite 2: Erste GAM
* Seite 3: Erster SGAM
* Seite 4: Unbenutzt
* Seite 5: Unbenutzt
* Seite 6: Erstes DCM
* Seite 7: Erstes BCM

#### Dateikopf

Die Seitennummer 0 aller Dateien enthält einen Header, der Metadaten über die Datei speichert.

#### Freier Speicherplatz auf Seite (PFS)
PFS identifiziert den Zuordnungsstatus und bestimmt die Menge an freiem Speicherplatz.

* Bit 1: Zeigt an, ob die Seite zugewiesen ist oder nicht.
* Bit 2: Gibt an, ob die Seite aus einem gemischten Extent stammt.
* Bit 3: Gibt an, dass diese Seite eine IAM-Seite ist.
* Bit 4: Zeigt an, dass diese Seite Geisteraufzeichnungen enthält
* Bits 5 bis 7: Ein kombinierter Drei-Bit-Wert, der die Seitenfülle wie folgt anzeigt:
* 0: Die Seite ist leer
* 1: Die Seite ist zu 1–50 % voll
* 2: Die Seite ist zu 51–80 % gefüllt
* 3: Die Seite ist zu 81–95 % gefüllt
* 4: Die Seite ist zu 96–100 % gefüllt

## Verweise

* [Datenbankdateien und Dateigruppen](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Datenbank trennen und anhängen – SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Anatomie der SQL Server-Datendatei analysieren](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

