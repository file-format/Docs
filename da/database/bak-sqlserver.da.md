{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"Microsoft SQL Server Database Backup",
"hvad er en bak-fil",
"hvordan man åbner bak fil",
"fil",
"bak filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK Filformat - Microsoft SQL Server Database Backup",
  "description": "Lær om BAK SQL Server Backup-format og API'er, der kan oprette og åbne BAK-filer.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-da",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Hvad er BAK fil?

En .bak-fil i forbindelse med Microsoft SQL Server er et backup-filformat, der bruges til at gemme kopier af en SQL Server-database. Disse filer indeholder et øjebliksbillede af databasen på et bestemt tidspunkt, inklusive dens skema, data og andre relaterede oplysninger. De genereres ved hjælp af SQL Servers indbyggede backup- og gendannelsesfunktionalitet og tjener flere afgørende formål:

1. **Datagendannelse:** .bak-filer giver mulighed for at gendanne en database i tilfælde af datatab, korruption eller andre problemer. Ved at gendanne en database fra en .bak-fil kan du vende den tilbage til en tidligere tilstand, hvilket minimerer nedetid og datatab.

2. **Migration og kloning:** Backup-filer bruges ofte til at migrere databaser mellem servere eller oprette kopier af databaser til test-, udviklings- eller rapporteringsformål. De tilbyder en ensartet og effektiv måde at flytte databaser mellem miljøer på.

3. **Point-in-Time Recovery:** SQL Server giver dig mulighed for at udføre point-in-time gendannelse ved hjælp af .bak-filer. Det betyder, at du kan gendanne en database til et bestemt tidspunkt, hvilket kan være afgørende for overholdelse af lovgivning eller datarevision.

4. **Disaster Recovery:** .bak-filer er en kritisk del af katastrofegendannelsesplanlægning. De sikrer, at dine data er sikre og hurtigt kan gendannes i tilfælde af hardwarefejl, naturkatastrofer eller andre katastrofale hændelser.

## Opret en .BAK-fil i SQL Server

For at oprette en .bak-fil i SQL Server bruger du typisk SQL Server Management Studio (SSMS) eller Transact-SQL (T-SQL) kommandoer som BACKUP DATABASE eller BACKUP LOG. Her er et forenklet eksempel på, hvordan du kan oprette en databasesikkerhedskopi ved hjælp af T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Gendan en .BAK-fil i SQL Server

For at gendanne en database fra en .bak-fil kan du bruge kommandoen RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Hvordan åbner man BAK fil i SQL Server?

For at åbne og få adgang til de data, der er gemt i en .bak-fil, skal du typisk gendanne den til en Microsoft SQL Server-instans. Her er de generelle trin til at åbne en .bak-fil ved hjælp af SQL Server Management Studio (SSMS):

1. **Start SQL Server Management Studio**: Åbn SSMS på din computer. Du kan normalt finde det i din startmenu eller ved at søge efter SQL Server Management Studio.

2. **Opret forbindelse til en SQL Server-instans**: I SSMS skal du oprette forbindelse til den SQL Server-instans, hvor du vil gendanne databasen. Du skal bruge de nødvendige tilladelser for at udføre denne handling.

3. **Gendan database**:

en. Udvid SQL Server-forekomsten i Objekt Explorer-ruden i venstre side.

b. Udvid noden Databaser.

c. Højreklik på Databaser og vælg Gendan database.

4. **Angiv kilde og destination**:

en. På siden Generelt i dialogboksen Gendan database skal du indtaste et navn til den nye database i feltet Til database. Dette vil være navnet på den gendannede database.

b. I afsnittet Kilde skal du vælge Enhed som backupmedietype.

c. Klik på knappen ... ved siden af feltet Enhed for at søge efter den .bak-fil, du vil gendanne.

d. Vælg den .bak-fil, du ønsker at åbne, og klik på OK.

5. **Gendannelsesindstillinger**: Gennemgå og konfigurer gendannelsesindstillingerne efter behov. Du kan angive, om en eksisterende database skal overskrives, indstille gendannelsesindstillinger og mere. Sørg for at indstille disse muligheder i overensstemmelse med dine krav.

6. **Start gendannelsen**: Når du har konfigureret gendannelsesindstillingerne, skal du klikke på knappen OK i dialogboksen Gendan database. SQL Server vil begynde gendannelsesprocessen.

7. **Få adgang til gendannet database**: Efter en vellykket gendannelse kan du få adgang til den gendannede database i SQL Server Management Studio ligesom enhver anden database. Du kan køre forespørgsler, se tabeller og arbejde med dataene i databasen.

## Andre BAK filer

Her er andre filtyper, der bruger filtypen **.bak**.

**Database**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**Spil**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Diverse**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Indstillinger**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Referencer
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
