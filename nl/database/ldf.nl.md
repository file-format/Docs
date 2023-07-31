{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over LDF-bestandsindelingen en API's die LDF-bestanden kunnen maken en openen.",
  "title" :"LDF - SQL Server Master Database-bestandsindeling",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een LDF-bestand?

Een bestand met de extensie .ldf is een logbestand dat wordt onderhouden door Microsoft SQL Server, een relationeel databasebeheersysteem (RDBMS). Alle transacties die worden uitgevoerd op primaire databasebestanden ([MDF](/nl/database/mdf/)) (zoals invoegen, bijwerken, verwijderen) worden vastgelegd in het LDF-bestand. LDF-bestanden zijn essentiële componenten van elke database. In het geval van een systeemstoring, wordt het logbestand gebruikt om de database in een consistente staat te herstellen. Het transactielogboekbestand kan groter worden als transacties niet volledig zijn vastgelegd. LDF-bestanden kunnen worden geopend met de Microsoft SQL Server-softwaretoepassing.

## Bewerkingen opgenomen in LDF-bestand

Een SQL-logbestand registreert de volgende bewerkingen:

* Het begin en einde van elke transactie.

* Elke wijziging van gegevensgegevens (invoegen, bijwerken of verwijderen). Dit omvat ook wijzigingen door op het systeem opgeslagen procedures of DDL-instructies (Data Definition Language) in elke tabel, inclusief systeemtabellen.

* Elke omvang en paginatoewijzing of deallocatie.

* Een tabel of index maken of neerzetten.

## LDF-bestandsindeling

Het LDF-bestand bestaat uit SQL Server-transactierecords die zijn gerangschikt als een reeks logboekrecords. Elk logboekrecord heeft een logboekvolgnummer (LSN) dat hoger is dan het LSN van het vorige record. De strings worden in het bestand na elkaar aaneengeschakeld. Dankzij de moderne hogesnelheidscomputers kunnen records worden ingevoegd waar de LSN2 in het logbestand vóór LSN1 bestaat. Omdat de bewerkingen in een serie worden vastgelegd, werd de door LSN2 beschreven wijziging uitgevoerd na het logrecord LSN1. De records voor een bepaalde transactie zijn achterwaarts gekoppeld met behulp van aanwijzers die worden gebruikt en het terugdraaien van de transactie versnellen.
 

## Referenties

* [Databasebestanden en bestandsgroepen](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Handleiding voor architectuur en beheer van transactielogboeken](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

