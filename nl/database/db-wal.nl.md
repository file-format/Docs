{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Leer meer over de DB-WAL-bestandsindeling en API's waarmee DB-WAL-bestanden kunnen worden gemaakt en geopend.",
  "title" : "DB-WAL-bestandsindeling - SQLite Database-schrijflogboekbestand",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-nl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Wat is een DB-WAL-bestand?

De bestandsextensie .db-wal wordt geassocieerd met SQLite, een populair open-source relationeel databasebeheersysteem. Het WAL-bestandsformaat (afkorting van Write-Ahead Log) is een alternatief voor het traditionele rollback-journaal dat door SQLite wordt gebruikt. Het biedt meer gelijktijdigheidscontrole, waardoor meerdere processen tegelijkertijd de database kunnen lezen, terwijl er nog steeds mogelijkheden voor crashherstel worden geboden. Het .db-wal-bestand wordt gebruikt om wijzigingen op te slaan die in de database zijn aangebracht en die nog niet zijn vastgelegd in het hoofddatabasebestand (met de extensie .db).

## Algemeen WAL-formaat

In het WAL-bestandsformaat (Write-Ahead Log) worden wijzigingen die in de database worden aangebracht eerst naar het WAL-bestand geschreven voordat ze in het hoofddatabasebestand worden vastgelegd. Dit maakt meer gelijktijdige toegang tot de database mogelijk, omdat meerdere processen uit de database kunnen lezen terwijl er wijzigingen worden aangebracht. Bovendien biedt het WAL-bestandsformaat mogelijkheden voor crashherstel, waardoor de database kan worden teruggezet naar een eerdere staat in het geval van een onverwachte afsluiting.

## Verschil tussen DB-WAL- en WAL-formaat

Zowel de .db-wal- als WAL-bestandsindelingen zijn gekoppeld aan SQLite, een populair open-source relationeel databasebeheersysteem. Er is echter een subtiel verschil tussen de twee.

Het .db-wal-bestand is in wezen een WAL-bestand, maar met een andere bestandsextensie. Het .db-wal-bestand wordt gebruikt om wijzigingen in de database op te slaan die nog niet zijn vastgelegd in het hoofddatabasebestand (met de extensie .db), terwijl het WAL-bestandsformaat wordt gebruikt om het vooruitschrijflogboek van de databasewijzigingen op te slaan .

Met andere woorden, een .db-wal-bestand is een specifiek type WAL-bestand dat door SQLite-databases wordt gebruikt om wijzigingen op te slaan die in de database zijn aangebracht en die nog niet in het hoofddatabasebestand zijn vastgelegd. Het WAL-bestandsformaat is de algemene term voor dit type bestandsformaat.

WAL is dus de algemene term voor het bestandsformaat, .db-wal is een specifieke implementatie van het WAL-bestandsformaat dat wordt gebruikt door SQLite-databases.

## Referenties
* [WAL-modus bestandsformaat](https://www.sqlite.org/walformat.html)

* [Write-Ahead Logging](https://www.sqlite.org/wal.html)


