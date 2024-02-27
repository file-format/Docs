{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"BAK Chromium Bogmærker",
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
  "title": "BAK-filformat - Chromium Bookmarks Backup",
  "description": "Lær om BAK Chromium Bookmarks-format og API'er, der kan oprette og åbne BAK-filer.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-da",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## Hvad er BAK fil?

En .bak-fil i forbindelse med Chromium-baserede webbrowsere, som Google Chrome og Microsoft Edge, er i bund og grund en sikkerhedskopi af dine bogmærker. Disse bogmærker gemmes som en almindelig tekstliste, og det anvendte filformat er JSON. Formålet med disse .bak-filer er at beskytte dine bogmærker ved at levere en sikkerhedskopi, der kan gendannes i tilfælde af utilsigtet sletning eller tab.

Chrom-baserede browsere, inklusive Google Chrome, opretter rutinemæssigt disse sikkerhedskopifiler og giver dem normalt navnet Bookmarks.bak. De er i bund og grund et øjebliksbillede af dine bogmærker på et bestemt tidspunkt.

## Sådan bruger du en .bak-fil til at gendanne dine bogmærker

1. **Find backupfilen:** Den er typisk placeret i en bestemt mappe, der er knyttet til din Chromium-profil. Den nøjagtige placering kan variere afhængigt af dit operativsystem.

På Windows: Se i `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

På macOS: Søg i `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

På Linux: Tjek `~/.config/chromium/Default/Bookmarks.bak`.

3. Sørg for, at din Chromium-browser er lukket.
4. Omdøb Bookmarks.bak-filen ved at fjerne .bak-udvidelsen, så den blot hedder Bookmarks.
5. Start Chromium.

Ved at omdøbe .bak-filen til Bogmærker, vil Chromium bruge den som den aktuelle bogmærkefil, og dine tidligere bogmærker bør gendannes.

## Chromium Bookmarks Backup

Sikkerhedskopiering af dine Chromium-bogmærker er en klog forholdsregel for at sikre, at du ikke mister dine vigtige gemte websider og webadresser. Chromium er en open source-browser, der fungerer som base for andre browsere som Google Chrome og Microsoft Edge. Følg disse trin for at sikkerhedskopiere dine Chromium-bogmærker:

## Metode 1: Manuel backup

1. **Åbn Chromium**: Start Chromium-browseren på din computer.

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **Vælg placering**: Vælg, hvor du vil gemme den eksporterede bogmærkefil på din computer. Standardfilnavnet er bookmarks.html, men du kan ændre det, hvis du foretrækker det. Gem det på et sted, du vil huske.

6. **Gem**: Klik på knappen Gem eller Eksporter for at gemme dine bogmærker som en HTML-fil.

Dine bogmærker er nu sikkerhedskopieret som en HTML-fil. Du kan kopiere denne fil til et eksternt drev eller skylager til opbevaring.

## Metode 2: Synkroniser med Google-konto (hvis relevant)

Hvis du er logget ind på en Google-konto i Chromium, kan du også bruge den indbyggede synkroniseringsfunktion til at holde dine bogmærker sikre og synkroniserede på tværs af enheder. På denne måde bliver dine bogmærker automatisk sikkerhedskopieret til din Google-konto.

1. **Åbn Chromium**: Start Chromium-browseren, og sørg for, at du er logget ind på din Google-konto.

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **Synkronisering og Google-tjenester**: På fanen Indstillinger skal du klikke på Synkronisering og Google-tjenester i venstre sidebjælke.

4. **Synkroniser dine data**: Under Synkroniser skal du sørge for, at Bogmærker er slået til. Dette vil synkronisere dine bogmærker med din Google-konto.

Dine bogmærker bliver nu automatisk sikkerhedskopieret og synkroniseret med din Google-konto. Du kan få adgang til dem ved at logge ind på din Google-konto på enhver enhed med Chromium eller en anden browser, der understøtter Google-synkronisering.

Husk også at sikkerhedskopiere dine bogmærker med jævne mellemrum, især hvis du ønsker en lokal kopi, der ikke udelukkende er afhængig af din Google-kontos synkronisering.

## Hvordan man åbner en BAK fil

Hvis du vil udforske rådataene i din bogmærke-sikkerhedskopi, kan du åbne filen Bookmarks.bak med forskellige teksteditorer såsom Microsoft Visual Studio Code (tilgængelig på flere platforme), Microsoft Notepad (til Windows-brugere), Apple TextEdit (for Mac-brugere) eller enhver anden teksteditor efter eget valg. Hvis du gør det, kan du se bogmærkerne og metadataene i filen.

Du kan åbne filen Bookmarks.bak og se dens indhold ved hjælp af forskellige tekstredigeringssoftware og kodeeditorer. Her er nogle almindeligt anvendte muligheder:

1. Visual Studio Code (VS Code)
2. Notesblok (Windows)
3. Tekstredigering (Mac)
4. Sublim tekst
5. Notesblok++
6. Atom
7. nano og Vim (Linux)
8. WordPad (Windows)

## Andre BAK filer

Her er andre filtyper, der bruger filtypen **.bak**.

**Database**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**Spil**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Diverse**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Indstillinger**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Referencer
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
