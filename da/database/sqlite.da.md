{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om SQLITE-filformat og API'er, der kan oprette og åbne SQLITE-filer.",
  "title": "SQLite filformat",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-dae"
}
},
  "lastmod": "2020-11-09"
}

## Hvad er en SQLite-fil?

En fil med filtypenavnet .sqlite er en letvægts SQL-databasefil, der er oprettet med [SQLite](https://www.sqlite.org/index.html)-softwaren. Det er en database i selve filen og implementerer en selvstændig, fuldt udstyret, yderst pålidelig [SQL](/database/sql/) databasemotor. SQLite-databasefiler kan bruges til at dele rigt indhold mellem systemer ved simpelt at udveksle disse filer over netværket. Næsten alle mobiler og computere bruger SQLite til lagring og deling af data, og er valget af filformat til applikationer på tværs af platforme. På grund af dens kompakte brug og nemme anvendelighed, kommer den med i andre applikationer. SQLite-bindinger findes for programmeringssprog såsom C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) og mange andre.

## SQLite filformat

SQLite er i virkeligheden et C-Language-bibliotek, der implementerer SQLite RDBMS ved hjælp af SQLite-filformatet. Med udviklingen af nye enheder hver eneste dag, er dets filformat blevet holdt bagudkompatibelt for at rumme ældre enheder. SQLite-filformat ses som langsigtet arkiveringsformat for dataene.

### Databasefilen

En SQLite-database vedligeholdes fuldt ud via to filer.
 * Hoveddatabasefil - Indeholder komplet tilstand af SQLite-databasen
 * Rollback Journal - Gemmer yderligere oplysninger i en anden fil og bruges under udførelse af transaktioner. Hvis SQLite er i WAL-tilstand, vedligeholdes en skrivehovedlogfil.

#### Journalfil

Denne fil er beregnet til at opbevare alle oplysningerne i tilfælde af, at den sidste transaktion ikke kunne gennemføres i tilfælde såsom et computernedbrud. Denne fil bruges til at gendanne databasefilen til en konsistent tilstand.

#### Sider

Den primære SQLite-databasefil består af en eller flere sider. På ethvert tidspunkt har hver side i hoveddatabasen en enkelt anvendelse, som er en af følgende:

 * Lås-byte-siden
 * En freelisteside
   * En friliste-stammeside
   * En freeliste-bladside
 * En b-træ side
   * En bord b-træ interiørside
   * En tabel b-træ bladside
   * En indeks b-træ interiørside
   * En indeks b-træ bladside
 * En nyttelastoverløbsside
 * En pointer-kortside

Størrelsen på SQLite-databasefiler kan variere fra få kilobyte til få gigabyte.

### SQLite Header

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Detaljer om overskriftsfelterne er som i følgende tabel.

|Offset|Størrelse|Beskrivelse|
---|---|---|
|0|16|Overskriftsstrengen: SQLite format 3\000|
|16|2|Databasens sidestørrelse i bytes. Skal være en potens af to mellem 512 og 32768 inklusive, eller værdien 1 repræsenterer en sidestørrelse på 65536.|
|18|1|Skriveversion af filformat. 1 for arv; 2 for WAL.|
|19|1|Læs version af filformat. 1 for arv; 2 for WAL.|
|20|1|Bytes af ubrugt reserveret plads i slutningen af hver side. Normalt 0.|
|21|1|Maksimal indlejret nyttelastbrøk. Skal være 64.|
|22|1|Minimum indlejret nyttelastbrøk. Skal være 32.|
|23|1|Løvnyttelastbrøk. Skal være 32.|
|24|4|Filændringstæller.|
|28|4|Størrelse på databasefilen i sider. In-header-databasestørrelsen.|
|32|4|Sidenummer på den første friliste-stammeside.|
|36|4|Samlet antal freelistesider.|
|40|4|Skema-cookien.|
|44|4|Skemaformatnummeret. Understøttede skemaformater er 1, 2, 3 og 4.|
|48|4|Standard sidecachestørrelse.|
|52|4|Sidenummeret på den største rod-b-træside, når den er i autovakuum- eller inkrementalvakuumtilstande, eller nul på anden måde.|
|56|4|The database text encoding. A value of 1 means UTF-8. En værdi på 2 betyder UTF-16le. En værdi på 3 betyder UTF-16be.|
|60|4|Brugerversionen som læst og indstillet af pragmaen user_version.|
|64|4|True (ikke-nul) for inkrementel vakuumtilstand. Falsk (nul) ellers.|
|68|4|Application ID indstillet af PRAGMA application_id.|
|72|20|Reserveret til udvidelse. Skal være nul.|
|92|4|Version-valid-for-nummeret.|
|96|4|SQLITE_VERSION_NUMBER|

## Referencer ##

* [SQLite-filformat - SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)

* [SQLite - C-sprogspecifikationer](https://www.sqlite.org/c3ref/intro.html)


