{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak fil",
"Handling! Database backup",
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
  "title": "BAK-filformat - Act! Database backup",
  "description": "Lær om BAK Act! Sikkerhedskopieringsformat og API'er, der kan oprette og åbne BAK-filer.",
  "linktitle": "BAK ACT Backup",
  "menu": {
    "docs": {
      "identifier": "database-bak-act-da",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Hvad er BAK fil?

En .BAK-fil fungerer også som en database-backupfil, der er genereret af Swiftpage Act!, som er en CRM-software (customer relationship management). Denne fil indeholder et duplikat af en Act! database (normalt en .ADF-fil), der effektivt bevarer væsentlige data såsom kundekontakter, virksomhedsoplysninger, gruppeoplysninger, noter, historiske optegnelser og aktivitetsdata gemt i databasen.

## Swiftpage Act!

Swiftpage Act! er en softwareapplikation, der bruges til kundeforholdsstyring (CRM). Det er designet til at hjælpe virksomheder og organisationer med at administrere deres kundeinteraktioner, spore salgs- og marketingaktiviteter og gemme vigtige kontaktoplysninger. Swiftpage Act! tilbyder funktioner såsom kontakthåndtering, e-mailmarketing, kalender- og opgavestyring, salgsautomatisering og rapportering for at strømline og forbedre processer til administration af kunderelationer.

Inden for Act! er alle kunderelaterede data gemt i en dedikeret databasefil, som kan sikkerhedskopieres efter Act! ledere og administratorer. Denne backup er især vigtig, når en virksomhed for eksempel planlægger at opgradere til en ny version af Act!. I sådanne tilfælde skal IT-administratoren, der er ansvarlig for Act! kan vælge at oprette en sikkerhedskopi af loven! database.

Disse lover! database backups gemmes i form af BAK filer. Under backup-processen er disse BAK-filer typisk bundtet i en [.ZIP](/compression/zip/)-fil. Dette ZIP-arkiv indeholder ikke kun kerneloven! database backup men omfatter også tilhørende Act! dataelementer, såsom vedhæftede dokumenter, dokumentskabeloner, rapportskabeloner og gemte databaseforespørgsler. Denne omfattende backup-tilgang sikrer, at kritiske kundeoplysninger og relaterede ressourcer er beskyttet og let kan gendannes, når det er nødvendigt.

## Hvordan åbner jeg filen BAK?

For at åbne en BAK-fil i Swiftpage Act! på et Windows-system kan du bruge Act! Diagnostik. Følg disse trin:

1. **Åben Act! Diagnostik**:
- Klik på Windows Start-menuen.
- Skriv 'actdiag' i søgefeltet.
- Tryk på Enter for at åbne Act! Diagnostik.

2. **Få adgang til Restore Database Tool**:
- Inden for handling! Diagnostik, naviger til menuen Værktøjer.

3. **Vælg Gendan database**:
- Under menuen Værktøjer skal du vælge Gendan database.

4. **Vælg Gendan BAK-fil**:
- Du vil blive præsenteret for to muligheder:
- For at overskrive en eksisterende database med dataene fra din BAK-fil, skal du vælge Gendan BAK-fil.
- For at tilføje din BAK-fil som en ny database sammen med eksisterende data, skal du vælge Gendan BAK-fil som.

5. **Følg vejledningen**:
- Handl! Diagnostik vil guide dig gennem processen med at gendanne databasen indeholdt i din BAK-fil.
- Du skal muligvis angive placeringen af BAK-filen og angive eventuelle yderligere indstillinger, der kræves til gendannelsen.

Følg disse trin, og handle! Diagnostics vil gendanne databasen fra din BAK-fil, så du kan få adgang til de data, der er gemt i den i Swiftpage Act!

## Andre BAK filer

Her er andre filtyper, der bruger filtypen **.bak**.

**Database**
- [BAK - Database Backup File](/database/bak/)
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

## Referencer
* [Swift Act!](https://en.wikipedia.org/wiki/Act!_LLC)
