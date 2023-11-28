{
"datum": "2023-06-12",
  "keywords": [
"bakken",
"bak-bestand",
"Microsoft SQL Server-databaseback-up",
"wat is een bak-bestand",
"hoe bak-bestand te openen",
"bestand",
"bak bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"BAK-bestandsindeling - Microsoft SQL Server-databaseback-up",
  "description":"Leer meer over het BAK SQL Server Backup-formaat en API's waarmee BAK-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent" : "database"
}
},
"laatste mod": "2023-06-12"
}

## Wat is een BAK-bestand?

Een ".bak"-bestand, in de context van Microsoft SQL Server, is een back-upbestandsformaat dat wordt gebruikt om kopieën van een SQL Server-database op te slaan. Deze bestanden bevatten een momentopname van de database op een specifiek tijdstip, inclusief het schema, de gegevens en andere gerelateerde informatie. Ze worden gegenereerd met behulp van de ingebouwde back-up- en herstelfunctionaliteit van SQL Server en dienen verschillende cruciale doeleinden:

1. **Gegevensherstel:** .bak-bestanden bieden een manier om een database te herstellen in geval van gegevensverlies, corruptie of andere problemen. Door een database te herstellen vanuit een .bak-bestand, kunt u deze terugzetten naar een eerdere staat, waardoor downtime en gegevensverlies tot een minimum worden beperkt.

2. **Migratie en klonen:** Back-upbestanden worden vaak gebruikt om databases tussen servers te migreren of kopieën van databases te maken voor test-, ontwikkelings- of rapportagedoeleinden. Ze bieden een consistente en efficiënte manier om databases tussen omgevingen te verplaatsen.

3. **Point-in-Time Recovery:** Met SQL Server kunt u point-in-time herstel uitvoeren met behulp van .bak-bestanden. Dit betekent dat u een database kunt herstellen naar een specifiek tijdstip, wat cruciaal kan zijn voor naleving van regelgeving of gegevensaudit.

4. **Herstel na noodgevallen:** .bak-bestanden vormen een cruciaal onderdeel van de planning voor herstel na een noodgeval. Ze zorgen ervoor dat uw gegevens veilig zijn en snel kunnen worden hersteld in het geval van hardwarestoringen, natuurrampen of andere catastrofale gebeurtenissen.

## Maak een .BAK-bestand in SQL Server

Als u een .bak-bestand in SQL Server wilt maken, gebruikt u doorgaans SQL Server Management Studio (SSMS) of Transact-SQL (T-SQL) opdrachten zoals BACKUP DATABASE of BACKUP LOG. Hier is een vereenvoudigd voorbeeld van hoe u een databaseback-up kunt maken met T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Herstel een .BAK-bestand in SQL Server

Om een database te herstellen vanuit een .bak-bestand, kunt u de opdracht RESTORE DATABASE gebruiken:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Hoe BAK-bestand openen in SQL Server?

Om de gegevens die zijn opgeslagen in een ".bak"-bestand te openen en te openen, moet u dit doorgaans herstellen naar een Microsoft SQL Server-exemplaar. Hier volgen de algemene stappen voor het openen van een ".bak"-bestand met behulp van SQL Server Management Studio (SSMS):

1. **Start SQL Server Management Studio**: Open SSMS op uw computer. U kunt het meestal vinden in uw Startmenu of door te zoeken naar 'SQL Server Management Studio'.

2. **Verbinding maken met een SQL Server-exemplaar**: maak in SSMS verbinding met het SQL Server-exemplaar waar u de database wilt herstellen. U heeft de benodigde machtigingen nodig om deze bewerking uit te voeren.

3. **Database herstellen**:

A. Vouw in het deelvenster Objectverkenner aan de linkerkant het SQL Server-exemplaar uit.

B. Vouw het knooppunt 'Databases' uit.

C. Klik met de rechtermuisknop op "Databases" en selecteer "Database herstellen".

4. **Geef bron en bestemming op**:

A. Voer op de pagina "Algemeen" van het dialoogvenster "Database herstellen" een naam in voor de nieuwe database in het veld "Naar database". Dit is de naam van de herstelde database.

B. Kies in het gedeelte 'Bron' 'Apparaat' als type back-upmedia.

C. Klik op de knop "..." naast het veld "Apparaat" om naar het ".bak"-bestand te bladeren dat u wilt herstellen.

D. Selecteer het ".bak"-bestand dat u wilt openen en klik op "OK".

5. **Herstelopties**: Bekijk en configureer de herstelopties indien nodig. U kunt opgeven of u een bestaande database wilt overschrijven, herstelopties wilt instellen en meer. Zorg ervoor dat u deze opties instelt op basis van uw vereisten.

6. **Start het herstel**: Nadat u de herstelopties heeft geconfigureerd, klikt u op de knop "OK" in het dialoogvenster "Database herstellen". SQL Server begint het herstelproces.

7. **Toegang tot herstelde database**: Na een succesvolle herstelbewerking hebt u net als elke andere database toegang tot de herstelde database in SQL Server Management Studio. U kunt query's uitvoeren, tabellen bekijken en met de gegevens in de database werken.

## Andere BAK-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.bak** gebruiken.

**Databank**
- [BAK - Databaseback-upbestand](/nl/database/bak/)
- [BAK - Swiftpage Act! Databaseback-up](/nl/database/bak-act/)

**Spel**
- [BAK - Terraria World of Spelerback-up](/nl/game/bak-terraria/)

**Overige**
- [BAK - Back-upbestand](/nl/misc/bak-backup/)
- [BAK - Back-up van Chromium-bladwijzers](/nl/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/nl/misc/bak-finale/)
- [BAK - MobileTrans Backup](/nl/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Back-up](/nl/misc/bak-vegas/)

**Instellingen**
- [BAK - Back-up van Holo Launcher] (/nl/settings/bak-holo/)

## Referenties
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
