{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par LDF failu formātu un API, kas var izveidot un atvērt LDF failus.",
  "title": "LDF — SQL servera galvenās datu bāzes faila formāts",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-lvf"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir LDF fails?

Fails ar paplašinājumu .ldf ir žurnālfails, ko uztur Microsoft SQL Server, kas ir relāciju datu bāzes pārvaldības sistēma (RDBMS). Visas primārajos datu bāzes failos ([MDF](/database/mdf/)) veiktās transakcijas (piemēram, ievietošana, atjaunināšana, dzēšana) tiek ierakstītas LDF failā. LDF faili ir svarīgas jebkuras datu bāzes sastāvdaļas. Sistēmas kļūmes gadījumā žurnāla fails tiek izmantots, lai atjaunotu datubāzes konsekventu stāvokli. Darījumu žurnālfaila lielums var palielināties, ja darījumi nav pilnībā saistīti. LDF failus var atvērt ar Microsoft SQL Server lietojumprogrammu.

## Operācijas ierakstītas LDF failā

SQL žurnāla fails ieraksta šādas darbības:

 * Katra darījuma sākums un beigas.

 * Katra datu datu modifikācija (ievietošana, atjaunināšana vai dzēšana). Tas ietver arī sistēmas saglabāto procedūru vai datu definīciju valodas (DDL) priekšrakstu izmaiņas jebkurā tabulā, tostarp sistēmas tabulās.

 * Jebkurš apjoms un lapu piešķiršana vai sadalīšana.

 * Tabulas vai indeksa izveide vai nomešana.

## LDF faila formāts

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Tā kā darbības tiek ierakstītas sērijveidā, LSN2 aprakstītās izmaiņas tika veiktas pēc žurnāla ieraksta LSN1. Konkrēta darījuma ieraksti tiek saistīti atpakaļ, izmantojot norādes, kas tiek izmantotas un paātrina darījuma atcelšanu.
 
## Atsauces

 * [Datu bāzes faili un failu grupas](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Transakciju žurnāla arhitektūras un pārvaldības rokasgrāmata](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -ver15)

