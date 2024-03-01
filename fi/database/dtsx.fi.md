{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
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
  "description": "Opi DTSX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DTSX-tiedostoja.",
  "title": "DTSX-tiedostomuoto - SQL Serverin DTS-asetustiedosto",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-fix"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on DTSX-tiedosto?

Tiedosto, jonka laajennus on .dtsx (Data Transformation Services Package XML), on Data Transformation Services (DTS) -tiedosto, jota Microsoft SQL käyttää viittaamaan tiedon siirron vaiheisiin/sääntöihin tiedon siirtämiseksi tietokannasta toiseen. Tämä sisältää muunnokset ja mahdolliset valinnaiset käsittelyvaiheet, joita voidaan tarvita tiedonsiirron aikana lähtö- ja kohdepisteiden välillä. SQL Server Integration Services (SSIS), Microsoft SQL Serverin osa, käyttää DTSX-tiedostoja tunnistaakseen vaiheet tietojen käsittelyssä tietokantapalvelinten välillä. DTSX-tiedostoja voidaan avata Microsoft SQL Server 2019:llä.

## DTSX tiedostomuoto

Tietojen siirtäminen tietokantapalvelinten välillä vaatii sääntöjä ja käsittelyvaiheita tietojen eheyden varmistamiseksi tämän toiminnon aikana. SSIS varmistaa, että kaikki nämä toiminnot eri lähteistä peräisin olevan tiedon siirtämiseksi ja mukauttamiseksi yrityksessä tapahtuvat kätevästi. Sieltä tulee DTSX, joka määrittelee rakenteet, joita SSIS käyttää määrittääkseen vaiheet, joissa tietoja voidaan käsitellä näiden vaiheiden kautta.

DTSX:n kuvaama tietovirta on seuraavan kuvan mukainen.

{{< figure src="../DataFlowDTSX.png" alt="Data Flow DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## Viitteet

 * [DTSX-muoto – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2 -muoto – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

