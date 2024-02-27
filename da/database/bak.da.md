{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"udvidelse",
"fil",
"filformat",
"BAK filtype",
"BAK filudvidelse",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om BAK filformat og API'er, der kan oprette og åbne BAK filer.",
  "title": "BAK filformat - Database backup fil",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-dak"
}
},
  "lastmod": "2020-12-04"
}

## Hvad er BAK fil?

En fil med filtypen .bak er normalt en sikkerhedskopifil, der bruges af forskellige softwareværktøjer til at gemme sikkerhedskopier af data. Fra databaseperspektiv bruges en BAK-fil af Microsoft SQL Server til lagring af indholdet af en database. Alle data og filer, der er knyttet til databasen, gemmes i dette filformat for at blive hentet i tilfælde af, at databasen kan blive korrupt eller ugyldig af en eller anden grund. Sikkerhedskopieringsfilerne kan gemmes og indekseres på andre servere af sikkerhedsmæssige årsager. Flere applikationer kan oprette BAK-filer såsom SQL Server Management Studio, Transact-SQL og Windows PowerShell.

## BAK filformat

De interne detaljer i en BAK-fil kendes ikke, men det er almindeligt antaget, at den er baseret på Microsoft Tape Format (MTF). MTF-specifikationer er tilgængelige og kan refereres til for at forstå strukturen af filen. Dokumentet giver detaljer om MTF-lagring for alle, der har en generel viden om lagerstyringsoperationer, bånddrev og filsystemer.

### Datasæt

Et datasæt er en samling af objekter skrevet til et lagermedie (bånd, optisk disk osv.) under sikkerhedskopiering eller gendannelse af data. Datasæt består af flere medier i tilfælde af store datamængder.

### Grundlæggende elementer i MTF

En MTF-fil består af nogle grundlæggende elementer, der udgør dens byggesten. Disse elementer er:

#### Deskriptorblokke

Deskriptorblokke (DBLK) bruges til formatkontrol og udgør det primære grundlag for en MTF-fil. En enkelt MTF-fil definerer flere DBLK'er for hver unik rolle. Hver DBLK er en datablok med variabel længde, der er opdelt i følgende fire dele:

 * `Common Block Header` - Struktur med fast længde, der er fælles for alle DBLK'er. Dette er den eneste blokoverskrift, som er påkrævet.
 * `DBLK Type Information` - Blok med fast længde, der er specifik for den type DBLK, der defineres
 * `Operating System Data` - Specifikke data, der er defineret baseret på typen af DBLK og operativsystemer
 * `DBLK Information` - DBLK-specifik information med variabel længde, som ikke kan gemmes med DBLK-informationen med fast længde.

{{< figure src=../bak.png alt=Microsoft SQL Backup File Format >}}

#### Datastrøm

Datastrømme i en MTF-fil bruges til dataindkapsling og justering. Den består af en Stream Header efterfulgt af Stream Data. En stream-header kan kun indkapsle en enkelt type streamdata.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL backup filformat" >}}

#### Filmærker

Et filmærke bruges til logisk adskillelse og hurtig adgang inden for et medie. Filmærker emuleres af enhedsdriveren eller ved brug af Soft Filemark Descriptor-blokken, hvis den anvendte enhed ikke leverer filmærker.

## Andre BAK filer

Her er andre filtyper, der bruger filtypen **.bak**.

**Database**
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

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

## Referencer ##

* [[MS-BCP]: Bulk Copy Format](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


