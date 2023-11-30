{
"datum": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"Act! Databas Backup",
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
"title": "BAK-filformat - Act! Database Backup",
  "description":"Läs mer om BAK Act! Backup-format och API:er som kan skapa och öppna BAK-filer.",
"linktitle": "BAK ACT Backup",
  "menu": {
    "docs": {
      "identifier": "database-bak-act",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Vad är BAK fil?

En .BAK-fil fungerar också som en säkerhetskopia av databas som genereras av Swiftpage Act!, som är en programvara för kundrelationshantering (CRM). Denna fil innehåller en dubblett av en Act! databas (vanligtvis en .ADF-fil), som effektivt bevarar viktiga data som kundkontakter, företagsinformation, gruppinformation, anteckningar, historiska register och aktivitetsdata lagrade i databasen.

## Swiftpage Act!

Swiftpage Act! är en mjukvaruapplikation som används för kundrelationshantering (CRM). Den är utformad för att hjälpa företag och organisationer att hantera sina kundinteraktioner, spåra försäljnings- och marknadsföringsaktiviteter och lagra viktig kontaktinformation. Swiftpage Act! erbjuder funktioner som kontakthantering, e-postmarknadsföring, kalender- och uppgiftshantering, försäljningsautomatisering och rapportering för att effektivisera och förbättra processer för hantering av kundrelationer.

Inom Act! lagras all kundrelaterad data i en dedikerad databasfil, som kan säkerhetskopieras efter eget gottfinnande av Act! chefer och administratörer. Denna säkerhetskopia är särskilt viktig när, till exempel, ett företag planerar att uppgradera till en ny version av Act!. I sådana fall ska IT-administratören som ansvarar för Act! kan välja att skapa en säkerhetskopia av lagen! databas.

Dessa agerar! säkerhetskopior av databas sparas i form av BAK-filer. Under säkerhetskopieringsprocessen buntas dessa BAK-filer vanligtvis till en [.ZIP](/sv/compression/zip/)-fil. Detta ZIP-arkiv innehåller inte bara kärnan Act! databassäkerhetskopiering men inkluderar även tillhörande Act! dataelement, såsom bifogade dokument, dokumentmallar, rapportmallar och sparade databasfrågor. Denna omfattande säkerhetskopieringsmetod säkerställer att kritisk kundinformation och relaterade resurser skyddas och lätt kan återställas vid behov.

## Hur öppnar man filen BAK?

För att öppna en BAK-fil i Swiftpage Act! på ett Windows-system kan du använda Act! Diagnostik. Följ dessa steg:

1. **Öppen akt! Diagnostik**:
- Klicka på Windows Start-menyn.
- Skriv 'actdiag' i sökfältet.
- Tryck på Enter för att öppna Act! Diagnostik.

2. **Åtkomst till verktyget för återställning av databas**:
– Inom Act! Diagnostik, navigera till menyn "Verktyg".

3. **Välj Återställ databas**:
- Under "Verktyg"-menyn, välj "Återställ databas."

4. **Välj Återställ BAK-fil**:
- Du kommer att presenteras med två alternativ:
- För att skriva över en befintlig databas med data från din BAK-fil, välj "Återställ BAK-fil."
- För att lägga till din BAK-fil som en ny databas tillsammans med befintliga data, välj "Återställ BAK-fil som."

5. **Följ anvisningarna**:
- Spela teater! Diagnostik guidar dig genom processen för att återställa databasen som finns i din BAK-fil.
- Du kan behöva ange platsen för BAK-filen och ange eventuella ytterligare inställningar som krävs för återställningen.

Följ dessa steg och agera! Diagnostik kommer att återställa databasen från din BAK-fil, så att du kan komma åt data som lagras i den i Swiftpage Act!

## Andra BAK-filer

Här är andra filtyper som använder filtillägget **.bak**.

**Databas**
- [BAK - Databasbackupfil](/sv/database/bak/)
- [BAK - Microsoft SQL Server Database Backup](/sv/database/bak-sqlserver/)

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
* [Swift Act!](https://en.wikipedia.org/wiki/Act!_LLC)
