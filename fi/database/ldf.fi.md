{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi LDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LDF-tiedostoja.",
  "title": "LDF - SQL Server Master Database -tiedostomuoto",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-fif"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on LDF-tiedosto?

Tiedosto, jonka laajennus on .ldf, on lokitiedosto, jota ylläpitää Microsoft SQL Server, joka on relaatiotietokannan hallintajärjestelmä (RDBMS). Kaikki ensisijaisessa tietokantatiedostossa ([MDF](/database/mdf/)) suoritetut tapahtumat (kuten lisäys, päivitys, poisto) tallennetaan LDF-tiedostoon. LDF-tiedostot ovat minkä tahansa tietokannan kriittisiä osia. Järjestelmävian sattuessa lokitiedostoa käytetään tietokannan palauttamiseen yhdenmukaiseen tilaan. Tapahtumalokitiedoston koko voi kasvaa, jos tapahtumat eivät ole täysin sitoutuneita. LDF-tiedostot voidaan avata Microsoft SQL Server -ohjelmistosovelluksella.

## Toiminnot tallennettu LDF-tiedostoon

SQL-lokitiedosto tallentaa seuraavat toiminnot:

 * Jokaisen tapahtuman alku ja loppu.

 * Jokainen datan muutos (lisää, päivitä tai poista). Tämä sisältää myös muutokset järjestelmään tallennettujen toimintojen tai DDL (Data Definition Language) -käskyjen avulla mihin tahansa taulukkoon, mukaan lukien järjestelmätaulukot.

 * Jokainen laajuus ja sivujen kohdistaminen tai jakelu.

 * Taulukon tai hakemiston luominen tai pudottaminen.

## LDF-tiedostomuoto

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Koska toiminnot tallennetaan sarjana, LSN2:n kuvaama muutos suoritettiin lokitietueen LSN1 jälkeen. Tietyn tapahtuman tietueet linkitetään taaksepäin käyttämällä osoittimia, jotka nopeuttavat tapahtuman palautusta.
 
## Viitteet

 * [Tietokantatiedostot ja tiedostoryhmät](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Tapahtumalokien arkkitehtuuri- ja hallintaopas](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -versio 15)

