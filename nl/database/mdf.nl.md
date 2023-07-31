{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MDF-bestandsindelingen en API's die MDF-bestanden kunnen maken en openen.",
  "title" :"MDF-bestandsindeling - SQL Server-hoofddatabasebestand",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een MDF-bestand?

Een bestand met de extensie .mdf is een hoofddatabasebestand dat door [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) wordt gebruikt om gebruikersgegevens op te slaan. Het is van het grootste belang omdat alle gegevens in dit bestand worden opgeslagen. Het MDF-bestand slaat gebruikersgegevens op in relationele databases in de formulierkolommen, rijen, velden, indexen, views en tabellen. Met SQL Server kunnen instellingen voor automatisch groeien en automatisch verkleinen worden ingesteld om een positieve invloed te hebben op de prestaties van de database. MDF-bestanden kunnen worden geladen en aan een database worden gekoppeld met behulp van Microsoft SQL Server. MDF-bestanden hebben het mime-type Application/octet-stream.

## MDF-bestandsindeling

De fundamentele eenheid van gegevensopslag in SQL Server is een pagina. Een aan een database toegewezen opslagpagina is verdeeld in logische pagina's met nummering van 0 tot n. Een enkele pagina begint met een header van 96 bytes die bestaat uit Pagina-ID, het type structuur waartoe de pagina behoort, het aantal records op de pagina en verwijzingen naar de vorige en volgende pagina's.

### Bestandsstructuur

Een MDF-bestand heeft de volgende gegevensstructuur.

* Pagina 0: Koptekst
* Pagina 1: Eerste PFS
* Pagina 2: Eerste GAM
* Pagina 3: Eerste SGAM
* Pagina 4: Ongebruikt
* Pagina 5: Ongebruikt
* Pagina 6: Eerste DCM
* Pagina 7: Eerste BCM

#### Bestandskoptekst

Het paginanummer 0 van alle bestanden bevat een header die metadata over het bestand opslaat.

#### Vrije paginaruimte (PFS)
PFS identificeert de toewijzingsstatus en bepaalt de hoeveelheid vrije ruimte.

* Bit 1: Geeft aan of de pagina is toegewezen of niet.
* Bit 2: Geeft aan of de pagina van een gemengd bereik is.
* Bit 3: Geeft aan dat deze pagina een IAM-pagina is.
* Bit 4: Geeft aan dat deze pagina spookrecords bevat
* Bits 5 tot 7: een gecombineerde waarde van drie bits, die de paginavolheid als volgt aangeeft:
* 0: De pagina is leeg
* 1: De pagina is 1–50% vol
* 2: De pagina is 51-80% vol
* 3: De pagina is voor 81-95% vol
* 4: De pagina is 96–100% vol

## Referenties

* [Databasebestanden en bestandsgroepen](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Database ontkoppelen en koppelen - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Anatomie van SQL Server-gegevensbestand analyseren](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

