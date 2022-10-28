{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MDF-Dateiformat und APIs, die NDF-Dateien erstellen und öffnen können.",
  "title" :"NDF-Dateiformat - SQL Server-Master-Datenbankdatei",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine NDF-Datei?

Eine Datei mit der Erweiterung .ndf ist eine sekundäre Datenbankdatei, die von [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) zum Speichern von Benutzerdaten verwendet wird. NDF ist eine sekundäre Speicherdatei, da der SQL-Server benutzerdefinierte Daten in einer primären Speicherdatei namens [MDF](/de/database/mdf/) speichert. Die NDF-Datendatei ist optional und benutzerdefiniert, um die Datenspeicherung zu verwalten, falls die primäre MDF-Datei den gesamten zugewiesenen Speicherplatz belegt. Es wird normalerweise auf einer separaten Festplatte gespeichert und kann sich auf mehrere Speichergeräte ausbreiten. Das Vorhandensein von MDF-Dateien ist erforderlich, um NDF-Dateien zu öffnen.

## NDF-Dateiformat

Das NDF-Dateiformat unterscheidet sich nicht von [MDF](/de/database/mdf) und verwendet Seiten als grundlegende Einheit der Datenspeicherung. Jede Seite beginnt mit einem 96-Byte-Header, der Folgendes enthält:

* Seiten-ID
* Art der Struktur
* Anzahl der Datensätze auf den Seiten
* Verweise auf vorherige und nächste Seiten

### NDF-Dateistruktur

Eine MDF-Datei hat die folgende Datenstruktur.

* Seite 0: Kopfzeile
* Seite 1: Erstes PFS
* Seite 2: Erste GAM
* Seite 3: Erster SGAM
* Seite 4: Unbenutzt
* Seite 5: Unbenutzt
* Seite 6: Erstes DCM
* Seite 7: Erstes BCM

#### Kopfzeile der NDF-Datei

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

## Datendateiseite

Seiten in einer SQL Server-Datendatei beginnen bei Null (0) und werden fortlaufend erhöht. Jede Datei wird durch eine eindeutige Datei-ID-Nummer erkannt. Das Paar aus Datei-ID und Seitenzahl identifiziert eine Seite in einer Datenbank eindeutig. Ein Beispiel, das Seitenzahlen in einer Datenbank zeigt, ist wie im folgenden Bild.

{{< figure src="../ndf.png" alt="NDF-Datenbankdateiformat" >}}

Dieses Beispiel zeigt Seitenzahlen in einer Datenbank mit einer primären Datendatei von 4 MB und einer sekundären Datendatei von 1 MB.

## Verweise

* [Datenbankdateien und Dateigruppen](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Datenbank trennen und anhängen – SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -Ver15)
* [Anatomie der SQL Server-Datendatei analysieren](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

