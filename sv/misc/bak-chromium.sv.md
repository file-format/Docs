{
"datum": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"BAK Chromium Bookmarks",
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
"title": "BAK-filformat - Chromium Bookmarks Backup",
  "description":"Läs mer om BAK Chromium Bookmarks-format och API:er som kan skapa och öppna BAK-filer.",
"linktitle": "BAK Chromium-bokmärken",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## Vad är BAK fil?

En .bak-fil i samband med Chromium-baserade webbläsare, som Google Chrome och Microsoft Edge, är i huvudsak en säkerhetskopia av dina bokmärken. Dessa bokmärken sparas som en vanlig textlista och filformatet som används är JSON. Syftet med dessa .bak-filer är att skydda dina bokmärken genom att tillhandahålla en säkerhetskopia som kan återställas i händelse av oavsiktlig radering eller förlust.

Krombaserade webbläsare, inklusive Google Chrome, skapar rutinmässigt dessa säkerhetskopior och ger dem vanligtvis namnet "Bookmarks.bak". De är i huvudsak en ögonblicksbild av dina bokmärken vid en viss tidpunkt.

## Hur man använder en .bak-fil för att återställa dina bokmärken

1. **Hitta säkerhetskopian:** Den finns vanligtvis i en specifik mapp som är kopplad till din Chromium-profil. Den exakta platsen kan variera beroende på ditt operativsystem.

På Windows: Titta i `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

På macOS: Sök i `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

På Linux: Kontrollera `~/.config/chromium/Default/Bookmarks.bak`.

3. Se till att din Chromium-webbläsare är stängd.
4. Byt namn på "Bookmarks.bak"-filen genom att ta bort tillägget ".bak", så att det helt enkelt kallas "Bookmarks".
5. Starta Chromium.

Genom att byta namn på .bak-filen till "Bokmärken" kommer Chromium att använda den som den aktuella bokmärkesfilen, och dina tidigare bokmärken bör återställas.

## Chromium Bookmarks Backup

Att säkerhetskopiera dina Chromium-bokmärken är en klok försiktighetsåtgärd för att säkerställa att du inte förlorar dina viktiga sparade webbsidor och webbadresser. Chromium är en webbläsare med öppen källkod som fungerar som bas för andra webbläsare som Google Chrome och Microsoft Edge. Följ dessa steg för att säkerhetskopiera dina Chromium-bokmärken:

## Metod 1: Manuell säkerhetskopiering

1. **Öppna Chromium**: Starta Chromium-webbläsaren på din dator.

2. **Åtkomst till bokmärken**: Klicka på de tre vertikala prickarna (menyikonen) i det övre högra hörnet av webbläsarfönstret. Håll muspekaren över "Bokmärken" från rullgardinsmenyn för att visa undermenyn för bokmärken.

3. **Exportera bokmärken**: Klicka på "Bokmärkshanteraren" i undermenyn för bokmärken. Detta öppnar en ny flik som visar dina bokmärken.

4. **Exportera bokmärken**: I bokmärkeshanterarens fliken klickar du på de tre vertikala prickarna igen (vanligtvis i det övre högra hörnet) för att öppna bokmärkshanterarens meny. Från den här menyn väljer du "Exportera bokmärken".

5. **Välj plats**: Välj var du vill spara den exporterade bokmärkesfilen på din dator. Standardfilnamnet är "bookmarks.html", men du kan ändra det om du föredrar det. Spara den på en plats du kommer ihåg.

6. **Spara**: Klicka på knappen "Spara" eller "Exportera" för att spara dina bokmärken som en HTML-fil.

Dina bokmärken har nu säkerhetskopierats som en HTML-fil. Du kan kopiera den här filen till en extern enhet eller molnlagring för förvaring.

## Metod 2: Synkronisera med Google-kontot (om tillämpligt)

Om du är inloggad på ett Google-konto i Chromium kan du också använda den inbyggda synkroniseringsfunktionen för att hålla dina bokmärken säkra och synkroniserade mellan enheter. På så sätt kommer dina bokmärken automatiskt att säkerhetskopieras till ditt Google-konto.

1. **Öppna Chromium**: Starta Chromium-webbläsaren och se till att du är inloggad på ditt Google-konto.

2. **Aktivera synkronisering**: Klicka på de tre vertikala prickarna (menyikonen) i det övre högra hörnet av webbläsarfönstret och gå till "Inställningar".

3. **Synkronisering och Google-tjänster**: På fliken Inställningar klickar du på "Synkronisering och Google-tjänster" i det vänstra sidofältet.

4. **Synkronisera dina data**: Se till att "Bokmärken" är aktiverat under "Synkronisera". Detta kommer att synkronisera dina bokmärken med ditt Google-konto.

Dina bokmärken kommer nu automatiskt att säkerhetskopieras och synkroniseras med ditt Google-konto. Du kan komma åt dem genom att logga in på ditt Google-konto på valfri enhet med Chromium eller annan webbläsare som stöder Google-synkronisering.

Kom ihåg att med jämna mellanrum säkerhetskopiera dina bokmärken manuellt också, särskilt om du vill ha en lokal kopia som inte enbart är beroende av synkroniseringen av ditt Google-konto.

## Hur man öppnar en BAK-fil

Om du vill utforska rådata för din säkerhetskopia av bokmärken kan du öppna filen "Bookmarks.bak" med olika textredigerare som Microsoft Visual Studio Code (tillgänglig på flera plattformar), Microsoft Notepad (för Windows-användare), Apple TextEdit (för Mac-användare), eller valfri annan textredigerare. Om du gör det kan du se bokmärkena och metadata som finns i filen.

Du kan öppna filen "Bookmarks.bak" och se dess innehåll med hjälp av olika textredigeringsprogram och kodredigerare. Här är några vanliga alternativ:

1. Visual Studio Code (VS Code)
2. Anteckningar (Windows)
3. Textredigering (Mac)
4. Sublim text
5. Anteckningar++
6. Atom
7. nano och Vim (Linux)
8. WordPad (Windows)

## Andra BAK-filer

Här är andra filtyper som använder filtillägget **.bak**.

**Databas**
- [BAK - Databasbackupfil](/sv/database/bak/)
- [BAK - Swiftpage Act! Databasbackup](/sv/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/sv/database/bak-sqlserver/)

**Spel**
- [BAK - Terraria World eller Player Backup](/sv/game/bak-terraria/)

**Övrigt**
- [BAK - Backup File](/sv/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/sv/misc/bak-finale/)
- [BAK - MobileTrans Backup](/sv/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/sv/misc/bak-vegas/)

**Inställningar**
- [BAK - Holo Launcher Backup](/sv/settings/bak-holo/)

## Referenser
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
