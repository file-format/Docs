{
"Datum": "12.06.2023",
  "keywords": [
"bak",
"bak-Datei",
"Microsoft SQL Server-Datenbanksicherung",
"Was ist eine Bak-Datei",
"Wie öffnet man eine Bak-Datei",
"Datei",
"bak-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
  "toc": true,
"title": "BAK-Dateiformat – Microsoft SQL Server-Datenbanksicherung",
  "description":"Erfahren Sie mehr über das BAK SQL Server Backup-Format und die APIs, mit denen BAK-Dateien erstellt und geöffnet werden können.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent": "database"
}
},
"lastmod": "12.06.2023"
}

## Was ist eine BAK-Datei?

Eine ".bak"-Datei ist im Kontext von Microsoft SQL Server ein Sicherungsdateiformat, das zum Speichern von Kopien einer SQL Server-Datenbank verwendet wird. Diese Dateien enthalten eine Momentaufnahme der Datenbank zu einem bestimmten Zeitpunkt, einschließlich Schema, Daten und anderen zugehörigen Informationen. Sie werden mithilfe der integrierten Sicherungs- und Wiederherstellungsfunktion von SQL Server generiert und dienen mehreren wichtigen Zwecken:

1. **Datenwiederherstellung:** .bak-Dateien bieten eine Möglichkeit, eine Datenbank im Falle von Datenverlust, Beschädigung oder anderen Problemen wiederherzustellen. Durch die Wiederherstellung einer Datenbank aus einer .bak-Datei können Sie sie auf einen früheren Zustand zurücksetzen und so Ausfallzeiten und Datenverluste minimieren.

2. **Migration und Klonen:** Sicherungsdateien werden häufig verwendet, um Datenbanken zwischen Servern zu migrieren oder Kopien von Datenbanken für Test-, Entwicklungs- oder Berichtszwecke zu erstellen. Sie bieten eine konsistente und effiziente Möglichkeit, Datenbanken zwischen Umgebungen zu verschieben.

3. **Point-in-Time-Wiederherstellung:** Mit SQL Server können Sie eine Point-in-Time-Wiederherstellung mithilfe von .bak-Dateien durchführen. Dies bedeutet, dass Sie eine Datenbank zu einem bestimmten Zeitpunkt wiederherstellen können, was für die Einhaltung gesetzlicher Vorschriften oder die Datenprüfung von entscheidender Bedeutung sein kann.

4. **Notfallwiederherstellung:** .bak-Dateien sind ein wichtiger Bestandteil der Notfallwiederherstellungsplanung. Sie sorgen dafür, dass Ihre Daten sicher sind und bei Hardwareausfällen, Naturkatastrophen oder anderen katastrophalen Ereignissen schnell wiederhergestellt werden können.

## Erstellen Sie eine .BAK-Datei in SQL Server

Um eine .bak-Datei in SQL Server zu erstellen, verwenden Sie normalerweise SQL Server Management Studio (SSMS) oder Transact-SQL (T-SQL)-Befehle wie BACKUP DATABASE oder BACKUP LOG. Hier ist ein vereinfachtes Beispiel dafür, wie Sie mit T-SQL eine Datenbanksicherung erstellen können:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Stellen Sie eine .BAK-Datei in SQL Server wieder her

Um eine Datenbank aus einer .bak-Datei wiederherzustellen, können Sie den Befehl RESTORE DATABASE verwenden:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Wie öffne ich eine BAK-Datei in SQL Server?

Um die in einer ".bak"-Datei gespeicherten Daten zu öffnen und darauf zuzugreifen, müssen Sie sie normalerweise auf einer Microsoft SQL Server-Instanz wiederherstellen. Hier sind die allgemeinen Schritte zum Öffnen einer ".bak"-Datei mit SQL Server Management Studio (SSMS):

1. **Starten Sie SQL Server Management Studio**: Öffnen Sie SSMS auf Ihrem Computer. Sie finden es normalerweise in Ihrem Startmenü oder indem Sie nach "SQL Server Management Studio" suchen.

2. **Mit einer SQL Server-Instanz verbinden**: Stellen Sie in SSMS eine Verbindung mit der SQL Server-Instanz her, in der Sie die Datenbank wiederherstellen möchten. Sie benötigen die erforderlichen Berechtigungen, um diesen Vorgang auszuführen.

3. **Datenbank wiederherstellen**:

A. Erweitern Sie im Objekt-Explorer-Bereich auf der linken Seite die SQL Server-Instanz.

B. Erweitern Sie den Knoten "Datenbanken".

C. Klicken Sie mit der rechten Maustaste auf "Datenbanken" und wählen Sie "Datenbank wiederherstellen".

4. **Quelle und Ziel angeben**:

A. Geben Sie auf der Seite "Allgemein" des Dialogfelds "Datenbank wiederherstellen" im Feld "Zur Datenbank" einen Namen für die neue Datenbank ein. Dies ist der Name der wiederhergestellten Datenbank.

B. Wählen Sie im Abschnitt "Quelle" als Backup-Medientyp "Gerät" aus.

C. Klicken Sie auf die Schaltfläche "…" neben dem Feld "Gerät", um nach der ".bak"-Datei zu suchen, die Sie wiederherstellen möchten.

D. Wählen Sie die ".bak"-Datei aus, die Sie öffnen möchten, und klicken Sie auf "OK".

5. **Wiederherstellungsoptionen**: Überprüfen und konfigurieren Sie die Wiederherstellungsoptionen nach Bedarf. Sie können angeben, ob eine vorhandene Datenbank überschrieben werden soll, Wiederherstellungsoptionen festlegen und vieles mehr. Stellen Sie sicher, dass Sie diese Optionen entsprechend Ihren Anforderungen einstellen.

6. **Initiieren Sie die Wiederherstellung**: Nachdem Sie die Wiederherstellungsoptionen konfiguriert haben, klicken Sie im Dialogfeld "Datenbank wiederherstellen" auf die Schaltfläche "OK". SQL Server beginnt mit dem Wiederherstellungsprozess.

7. **Zugriff auf wiederhergestellte Datenbank**: Nach einer erfolgreichen Wiederherstellung können Sie wie auf jede andere Datenbank in SQL Server Management Studio auf die wiederhergestellte Datenbank zugreifen. Sie können Abfragen ausführen, Tabellen anzeigen und mit den Daten in der Datenbank arbeiten.

## Andere BAK-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.bak** verwenden.

**Datenbank**
- [BAK – Datenbanksicherungsdatei](/database/bak/)
- [BAK – Swiftpage Act! Datenbanksicherung](/database/bak-act/)

**Spiel**
- [BAK – Terraria World oder Player Backup](/game/bak-terraria/)

**Verschiedenes**
- [BAK – Sicherungsdatei](/misc/bak-backup/)
- [BAK – Chromium-Lesezeichen-Backup](/misc/bak-chromium/)
- [BAK – Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK – MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK – VEGAS Videoprojekt-Backup](/misc/bak-vegas/)

**Einstellungen**
- [BAK – Holo Launcher Backup](/settings/bak-holo/)

## Verweise
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
