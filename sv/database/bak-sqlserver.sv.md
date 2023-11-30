{
"datum": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"Microsoft SQL Server Database Backup",
"vad är en bak-fil",
"hur man öppnar bak-fil",
"fil",
"bak filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK-filformat - Microsoft SQL Server Database Backup",
  "description":"Läs mer om BAK SQL Server Backup-format och API:er som kan skapa och öppna BAK-filer.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Vad är BAK fil?

En ".bak"-fil, i Microsoft SQL Server-sammanhang, är ett backupfilformat som används för att lagra kopior av en SQL Server-databas. Dessa filer innehåller en ögonblicksbild av databasen vid en specifik tidpunkt, inklusive dess schema, data och annan relaterad information. De genereras med hjälp av SQL Servers inbyggda säkerhetskopierings- och återställningsfunktionalitet och tjänar flera avgörande syften:

1. **Dataåterställning:** .bak-filer är ett sätt att återställa en databas i händelse av dataförlust, korruption eller andra problem. Genom att återställa en databas från en .bak-fil kan du återställa den till ett tidigare tillstånd, vilket minimerar driftstopp och dataförlust.

2. **Migrering och kloning:** Säkerhetskopieringsfiler används ofta för att migrera databaser mellan servrar eller skapa kopior av databaser för test-, utvecklings- eller rapporteringsändamål. De erbjuder ett konsekvent och effektivt sätt att flytta databaser mellan miljöer.

3. **Point-in-Time Recovery:** SQL Server låter dig utföra punkt-i-tid återställning med hjälp av .bak-filer. Detta innebär att du kan återställa en databas till ett specifikt ögonblick, vilket kan vara avgörande för regelefterlevnad eller datarevision.

4. **Återställning efter katastrof:** .bak-filer är en viktig del av planering av katastrofåterställning. De säkerställer att dina data är säkra och kan återställas snabbt i händelse av hårdvarufel, naturkatastrofer eller andra katastrofala händelser.

## Skapa en .BAK-fil i SQL Server

För att skapa en .bak-fil i SQL Server använder du vanligtvis SQL Server Management Studio (SSMS) eller Transact-SQL (T-SQL) kommandon som BACKUP DATABASE eller BACKUP LOG. Här är ett förenklat exempel på hur du kan skapa en databassäkerhetskopiering med T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Återställ en .BAK-fil i SQL Server

För att återställa en databas från en .bak-fil kan du använda kommandot RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Hur öppnar man en BAK-fil i SQL Server?

För att öppna och komma åt data som lagras i en ".bak"-fil måste du vanligtvis återställa den till en Microsoft SQL Server-instans. Här är de allmänna stegen för att öppna en ".bak"-fil med SQL Server Management Studio (SSMS):

1. **Starta SQL Server Management Studio**: Öppna SSMS på din dator. Du kan vanligtvis hitta den i din Start-meny eller genom att söka efter "SQL Server Management Studio."

2. **Anslut till en SQL Server-instans**: I SSMS, anslut till SQL Server-instansen där du vill återställa databasen. Du behöver de nödvändiga behörigheterna för att utföra denna operation.

3. **Återställ databas**:

a. Expandera SQL Server-instansen i objektutforskaren på vänster sida.

b. Expandera noden "Databaser".

c. Högerklicka på "Databaser" och välj "Återställ databas".

4. **Ange källa och destination**:

a. På sidan "Allmänt" i dialogrutan "Återställ databas" anger du ett namn för den nya databasen i fältet "Till databas". Detta kommer att vara namnet på den återställda databasen.

b. I avsnittet "Källa" väljer du "Enhet" som backup-mediatyp.

c. Klicka på knappen "..." bredvid fältet "Enhet" för att söka efter filen ".bak" som du vill återställa.

d. Välj ".bak"-filen du vill öppna och klicka på "OK".

5. **Återställningsalternativ**: Granska och konfigurera återställningsalternativen efter behov. Du kan ange om en befintlig databas ska skrivas över, ställa in återställningsalternativ och mer. Se till att ställa in dessa alternativ enligt dina krav.

6. **Starta återställningen**: När du har konfigurerat återställningsalternativen klickar du på knappen "OK" i dialogrutan "Återställ databas". SQL Server kommer att påbörja återställningsprocessen.

7. **Åtkomst till återställd databas**: Efter en lyckad återställning kan du komma åt den återställda databasen i SQL Server Management Studio precis som vilken annan databas som helst. Du kan köra frågor, visa tabeller och arbeta med data i databasen.

## Andra BAK-filer

Här är andra filtyper som använder filtillägget **.bak**.

**Databas**
- [BAK - Databasbackupfil](/sv/database/bak/)
- [BAK - Swiftpage Act! Databasbackup](/sv/database/bak-act/)

**Spel**
- [BAK - Terraria World eller Player Backup](/sv/game/bak-terraria/)

**Övrigt**
- [BAK - Backup File](/sv/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/sv/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/sv/misc/bak-finale/)
- [BAK - MobileTrans Backup](/sv/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/sv/misc/bak-vegas/)

**Inställningar**
- [BAK - Holo Launcher Backup](/sv/settings/bak-holo/)

## Referenser
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
