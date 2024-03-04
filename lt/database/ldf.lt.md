{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie LDF failo formatą ir API, kurios gali kurti ir atidaryti LDF failus.",
  "title": "LDF – SQL serverio pagrindinės duomenų bazės failo formatas",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-ltf"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra LDF failas?

Failas su plėtiniu .ldf yra žurnalo failas, kurį tvarko Microsoft SQL Server, kuris yra reliacinė duomenų bazių valdymo sistema (RDBMS). Visos operacijos, atliktos su pirminiais duomenų bazės failais ([MDF](/database/mdf/)) (pvz., įterpimas, atnaujinimas, ištrynimas), įrašomos į LDF failą. LDF failai yra svarbūs bet kurios duomenų bazės komponentai. Sistemos gedimo atveju žurnalo failas naudojamas atkurti duomenų bazę į nuoseklią būseną. Operacijų žurnalo failo dydis gali padidėti, jei operacijos nėra visiškai įtrauktos. LDF failus galima atidaryti naudojant Microsoft SQL Server programinę įrangą.

## Operacijos įrašytos į LDF failą

SQL žurnalo faile įrašomos šios operacijos:

 * Kiekvienos operacijos pradžia ir pabaiga.

 * Kiekvienas duomenų duomenų modifikavimas (įterpimas, atnaujinimas arba ištrynimas). Tai taip pat apima sistemos saugomų procedūrų arba duomenų apibrėžimo kalbos (DDL) teiginių pakeitimus bet kurioje lentelėje, įskaitant sistemos lenteles.

 * Kiekvienas mastas ir puslapio paskirstymas arba paskirstymas.

 * Lentelės ar rodyklės kūrimas arba išmetimas.

## LDF failo formatas

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Kadangi operacijos įrašomos serijiniu būdu, LSN2 aprašytas pakeitimas buvo atliktas po žurnalo įrašo LSN1. Konkrečios operacijos įrašai susiejami atgal, naudojant nuorodas, kurios yra naudojamos ir pagreitina operacijos atšaukimą.
 
## Nuorodos

 * [Duomenų bazių failai ir failų grupės](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Operacijų žurnalo architektūros ir valdymo vadovas](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -15 versija)

