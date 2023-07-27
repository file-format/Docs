{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MDF-bestandsindelingen en API's die NDF-bestanden kunnen maken en openen.",
  "title" :"NDF-bestandsindeling - SQL Server-hoofddatabasebestand",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een NDF-bestand?

Een bestand met de extensie .ndf is een secundair databasebestand dat door [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) wordt gebruikt om gebruikersgegevens op te slaan. NDF is een secundair opslagbestand omdat de SQL-server door de gebruiker gespecificeerde gegevens opslaat in een primair opslagbestand dat bekend staat als [MDF](/nl/database/mdf/). NDF-gegevensbestand is optioneel en wordt door de gebruiker gedefinieerd om gegevensopslag te beheren in het geval dat het primaire MDF-bestand alle toegewezen ruimte in beslag neemt. Het wordt meestal op een aparte schijf opgeslagen en kan zich verspreiden naar meerdere opslagapparaten. De aanwezigheid van MDF-bestanden is noodzakelijk om NDF-bestanden te openen.

## NDF-bestandsindeling

Het NDF-bestandsformaat is niet anders dan [MDF](/nl/database/mdf/) en gebruikt pagina's als de fundamentele eenheid van gegevensopslag. elke pagina begint met een header van 96 bytes die het volgende omvat:

* Pagina-ID
* Type structuur
* Aantal records in de pagina's
* Verwijzingen naar vorige en volgende pagina's

### NDF-bestandsstructuur

Een MDF-bestand heeft de volgende gegevensstructuur.

* Pagina 0: Koptekst
* Pagina 1: Eerste PFS
* Pagina 2: Eerste GAM
* Pagina 3: Eerste SGAM
* Pagina 4: Ongebruikt
* Pagina 5: Ongebruikt
* Pagina 6: Eerste DCM
* Pagina 7: Eerste BCM

#### NDF-bestandskop

Het paginanummer 0 van alle bestanden bevat een header die metadata over het bestand opslaat.

#### Vrije paginaruimte (PFS)
PFS identificeert de toewijzingsstatus en bepaalt de hoeveelheid vrije ruimte.

* Bit 1: Geeft aan of de pagina is toegewezen of niet.
* Bit 2: Geeft aan of de pagina van een gemengd bereik is.
* Bit 3: Geeft aan dat deze pagina een IAM-pagina is.
* Bit 4: Geeft aan dat deze pagina spookrecords bevat
* Bits 5 tot 7: een gecombineerde drie-bits waarde, die de pagina volheid als volgt aangeeft:
* 0: De pagina is leeg
* 1: De pagina is 1–50% vol
* 2: De pagina is 51-80% vol
* 3: De pagina is voor 81-95% vol
* 4: De pagina is 96–100% vol

## Gegevensbestandspagina

Pagina's in een SQL Server-gegevensbestand beginnen bij nul (0) en worden opeenvolgend verhoogd. Elk bestand wordt herkend aan een uniek bestands-ID-nummer. Het paar bestands-ID en paginanummer identificeert op unieke wijze een pagina in een database. Een voorbeeld van paginanummers in een database, is zoals in de volgende afbeelding.

{{< figure src="../ndf.png" alt="NDF-databasebestandsindeling" >}}

Dit voorbeeld toont paginanummers in een database met een primair gegevensbestand van 4 MB en een secundair gegevensbestand van 1 MB.

## Referenties

* [Databasebestanden en bestandsgroepen](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Database ontkoppelen en koppelen - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Anatomie van SQL Server-gegevensbestand analyseren](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

