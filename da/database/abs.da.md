{
  "date" : "2023-06-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om ABS-filformat og API'er, der kan oprette og åbne ABS-filer.",
  "title" : "ABS-filudvidelse - Delphi Absolute Database-filformat",
  "linktitle" : "ABS",
  "menu" : {
    "docs" : {
      "identifier":"database-abs-da",
      "parent" : "database"
}
},
  "lastmod" : "2023-06-18"
}

## Hvad er ABS fil?

En fil med filtypenavnet .abs er en database, der genereres og bruges af Absolute-databasen, som er en databasemotor til Delphi-softwareudviklingens IDE. Den erstattede Borland Database Engine (DBE) og er mere kompakt, højhastigheds, robust og nem at bruge. ABS-databasen kompileres som en del af applikationens EXE-fil, hvilket gør din applikation hurtigere og mindre. Data gemmes i en ABS-fil i et struktureret, relationelt format.

## ABS-filformat - flere oplysninger

ABS-filer er lagret som en del af applikationens [EXE file](/executable/exe/), som normalt gemmes som en binær fil. Binære filer kan ikke åbnes i nogen teksteditor og giver hurtig adgang til indholdet af databasefilen.

### Nøglefunktioner i ABS-filformat

ABS-filer er ret enkle og integreres i programmets eksekverbare. Den har følgende funktioner:

 * Ingen BDE; ingen DLL'er
 * Enkelt-fil database
 * SQL'92 (DDL & DML) understøttelse
 * Kompatibel med standard- og tredjeparts-databasekontroller
 * Enkeltbruger- og flerbrugertilstand (filserver)
 * Fungerer godt på alle versioner af Windows - fra 98 til den nyeste, kræver ingen opdateringer eller servicepakker
 * Ultrahurtige hukommelsestabeller
 * Uovertruffen brugervenlighed
 * Stærk kryptering
 * BLOB kompression
 * Gratis til personlig brug
 * Fuld kildekode tilgængelig
 * Royalty-fri distribution

## Referencer

 * [Delphi Absolute Database File Format](https://www.componentace.com/bde_replacement_database_delphi_absolute_database.htm)
