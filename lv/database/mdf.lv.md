{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "Uzziniet par MDF failu formātu un API, kas var izveidot un atvērt MDF failus.",
  "title": "MDF faila formāts — SQL servera galvenā datu bāzes fails",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-lvf"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir MDF fails?

Fails ar paplašinājumu .mdf ir galvenais datu bāzes fails, ko izmanto [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server), lai saglabātu lietotāja datus. Tas ir ļoti svarīgi, jo visi dati tiek glabāti šajā failā. MDF fails saglabā lietotāju datus relāciju datu bāzēs veidlapu kolonnās, rindās, laukos, indeksos, skatos un tabulās. SQL Server ļauj iestatīt automātiskās izaugsmes un automātiskās samazināšanas iestatījumus, lai tie pozitīvi ietekmētu datu bāzes veiktspēju. MDF failus var ielādēt un pievienot datu bāzei, izmantojot Microsoft SQL Server. MDF failiem ir lietojumprogrammas/okteta straumes mime tips.

## MDF faila formāts

SQL Server datu glabāšanas pamatvienība ir lapa. Datubāzei piešķirtā krātuves lapa ir sadalīta loģiskās lapās ar numuru no 0 līdz n. Viena lapa sākas ar 96 baitu galveni, kas sastāv no lapas ID, struktūras veida, kurai lapa pieder, ierakstu skaita lapā un norādes uz iepriekšējo un nākamo lapu.

### Faila struktūra

MDF failam ir šāda datu struktūra.

 * 0. lapa: galvene
 * 1. lapa: pirmais PFS
 * 2. lapa: Pirmā GAM
 * 3. lapa: pirmais SGAM
 * 4. lapa: Nelietots
 * 5. lapa: Nelietots
 * 6. lapa: pirmais DCM
 * 7. lapa: pirmais BCM

#### Faila galvene

Visu failu lappuses numurs 0 satur galvenes, kas glabā metadatus par failu.

#### Lapas brīva vieta (PFS)
PFS identificē piešķiršanas statusu un nosaka brīvās vietas daudzumu.

 * 1. bits: norāda, vai lapa ir piešķirta vai nav.
 * 2. bits: norāda, vai lapa ir no jaukta apjoma.
 * 3. bits: norāda, ka šī lapa ir IAM lapa.
 * 4. bits: norāda, ka šajā lapā ir spoku ieraksti
 * Biti no 5 līdz 7: apvienota trīs bitu vērtība, kas norāda lapas pilnību šādi:
   * 0: lapa ir tukša
   * 1: lapa ir pilna par 1–50%.
   * 2: lapa ir pilna par 51–80%.
   * 3: lapa ir pilna par 81–95%.
   * 4: lapa ir pilna par 96–100%.

## Atsauces

 * [Datu bāzes faili un failu grupas](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Datu bāzes atdalīšana un pievienošana — SQL serveris](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- versija 15)
 * [SQL servera datu faila anatomijas analīze](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

